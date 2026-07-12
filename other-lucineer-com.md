# lucineer-com

## Intention

Structured lucid dream practice tool — evidence-based techniques, dream sign tracking, and progress analytics at lucineer.com

## How It Works

**Architecture**: Single Cloudflare Worker serving complete HTML with inline CSS. The page is a static document rendered on every request — no client framework, no API calls. This delivers the fastest possible load time: sub-50ms globally via Cloudflare's edge network.
**Content design**: The application is organized around the practice loop:
```
Observe → Identify Dream Signs → Set Triggers → Practice → Measure → Adjust
```
**Core sections**:
1. **Technique library** — three pillars with citations:
- **Reality Testing (RCT)**: Nose pinch, finger-through-palm, text reread. Evidence: LaBerge & Rheingold, 1990.
- **WBTB (Wake Back to Bed)**: Alarm at 4.5-5h, wake 15-20 min, review journal, return to sleep. Evidence: Stumbrys et al., 2012.
- **SSILD (Senses Initiated Lucid Dream)**: Post-WBTB, cycle through visual/auditory/tactile focus 4-5 times. Community-developed, widely validated.
2. **Dream sign tracker** — recurring elements with occurrence counts:
- "Houses with impossible rooms" → 11 occurrences
- "Water where it shouldn't be" → 9 occurrences
- "High school people, wrong context" → 7 occurrences
These are the user's personal triggers. When encountered while awake → reality check.

## What It's For

Structured lucid dream practice tool — evidence-based techniques, dream sign tracking, and progress analytics at lucineer.com

## Who Would Use It

Developers and researchers in the SuperInstance ecosystem. Those building systems that need this specific computational primitive.

## Language / Stack

- **Primary language:** TypeScript

## Status Assessment

**Status: LIGHT**

Short README (48 lines), mentions tests, includes examples.

- README length: 76 lines, 4975 characters
- Documented sections: Why It Matters, How It Works, Quick Start, API, Architecture Notes

## Honest Assessment

Some documentation exists but it's not comprehensive. The project may have working code, but the README doesn't provide enough evidence of maturity, testing, or real-world use. **Promising direction, needs more evidence of substance.**
