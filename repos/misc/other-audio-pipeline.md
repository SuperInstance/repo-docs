# audio-pipeline

**Cluster:** infra-devops  
**Language:** Rust  
**Source:** [SuperInstance/audio-pipeline](https://github.com/SuperInstance/audio-pipeline)

## Intention

Audio processing pipeline - transcoding, streaming, and analysis for voice applications

## How It Works

audio-pipeline follows the **"Audio streams become conversational signals"** philosophy:

[code]

### Core Abstractions

1. **AudioStream**: Continuous audio capture
   [code]

2. **VADDetector**: Voice activity detection
   [code]

3. **ASREngine**: Automatic speech recognition
   [code]

4. **SentimentAnalyzer**: Sentiment from audio
   [code]

## What It's For

Audio processing pipeline - transcoding, streaming, and analysis for voice applications

## Who Would Use It

Developers and researchers in the SuperInstance fleet ecosystem.

## Language / Stack

Rust — part of the SuperInstance ecosystem.

## Status Assessment

- **Quality tier:** substantial
- **Note:** Rich documentation (304 lines, 8759 chars). Architecture + motivation.

## Honest Assessment

Rich documentation with architecture, motivation, and code. Among the more serious projects. AI-created as part of agent fleet infrastructure, but with genuine depth and thinking.

## README Excerpt

```
# audio-pipeline

**Real-time audio processing for conversational interruption detection**

audio-pipeline is a high-performance Rust/Python library that processes audio streams in real-time, enabling <5ms interruption detection for the equilibrium-tokens architecture. By leveraging Voice Activity Detection (VAD), Automatic Speech Recognition (ASR), and sentiment analysis, audio-pipeline transforms raw audio streams into conversational signals.

## Performance Highlights

- **VAD Latency**: <1ms (Silero VAD on CPU)
- **ASR Latency**: <100ms end-to-end (CAIMAN-ASR streaming)
- **Sentiment Analysis**: <5ms with GPU acceleration
- **Throughput**: >100K audio frames/second
- **Accuracy**: >99% speech detection, <10% word error rate

## Key Features

### 1. Voice Activity Detection (VAD)
- **Silero VAD**: <1ms inference, 99.5% accuracy
- **WebRTC VAD**: Open-source fallback, 95% accuracy
- **AtomicVAD**: Ultra-lightweight model (experimental)
- Multi-speaker detection support

### 2. Automatic Speech Recognition (ASR)
- **CAIMAN-ASR**: 4× lower latency than competitors, streaming capable
- **Whisper**: Fallback option with higher accuracy
- Real-time transcription with <100ms latency
- Word error rate <10%

### 3. Sentiment from Audio
- GPU-accelerated VAD (Valence-Arousal-Dominance) scoring
- <5ms inference with CUDA Graph acceleration
- >85% valence classification accuracy
- Parallel processing with VAD/ASR

### 4. Stream Processing
- Continuous audio capture from microphone or API
- Ring buffer architecture (1 second default)
- 32ms frame processing (512 samples at 16kHz)
- Lock-free data structures for real-time performance

## Integration with equilibrium-tokens

audio-pipeline is the primary signal source for the **Interruption Equilibrium Surface**, enabling the system to detect user interruptions in real-time:

```rust
use audio_pipeline::{AudioStream, VADDetector, ASREngine};
use equilibrium_tokens::InterruptionEquilibrium;

// Detect interruptions from voice
let mut audio_stream = AudioStream::new(Hz(16000), SampleFormat::F32)?;
let mut vad = VADDetector::silero()?;  // <1ms
let asr = ASREngine::caiman()?;         // <100ms
let interruption_surface = InterruptionEquilibrium::new()?;

loop {
    // Wait for next audio frame (32ms at 16kHz)
    let frame = audio_stream.next_frame().await?;

    // VAD: <1ms
    if vad.detect(&frame)?.is_speech {
        // ASR: <100ms (streaming)
        if let Ok(text) = asr.transcribe(&frame) {
            // Check if interruption
            if is_interruption(&text) {
                interruption_surface.reset_attention().await?;
            }
        }
    }
}
```

## Timeless Foundation

audio-pipeline is built on the **Nyquist-Shannon sampling theorem**:

```rust
// To capture frequency f, sample rate must be > 2f
const MAX_SPEECH_FREQUENCY: Hz = Hz(8000);  // 8kHz max for speech
const MIN_SAMPLE_RATE: Hz = Hz(16000);      // 16kHz (2 × 8kHz)

// 16 kHz is the timeless standard for speech audio
```

Thi
```
