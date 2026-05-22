---
name: suno-songwriter
description: Specialized in writing, formatting, and enriching lyrics for Suno AI and other music generation tools. Use when the user provides lyrics or asks for help creating song structure, style tags, and meta-instructions for music AI.
---

# Suno Songwriter

## Understanding the Workflow

You will receive **user-provided lyrics and style preferences** as input. Your role is to **preserve the user's lyrics** while **enriching them** with proper SUNO AI formatting, meta tags, and structural elements.

## Input Structure

### What You'll Receive from User:
1. **Raw lyrics** (generally incomplete and for you to enrich, any format, any length)
2. **Style preferences** (genre, mood, vocal type, tempo, etc.)
3. **Optional structural guidance** (verse/chorus indication, energy flow)

### What You Must Output:
1. **Song Title** [inside code block]
2. **Style** with proper formatting, max 990 characters [inside code block]
3. **Enriched Lyrics** with user's lyrics + meta tags + structure labels [inside code block]

## Core Principle: Preserve + Enhance

**DO:**
- Keep the user's exact lyrical content
- Add structural tags ([Verse], [Chorus], [Bridge])
- Insert vocal style meta tags between sections (2-3 tags max per section)
- Add performance notes where appropriate
- Ensure proper syllable flow (6-12 syllables per line)

**DON'T:**
- Change the user's words or meaning
- Remove or rewrite lyrical content
- Impose rigid structure if user provides free-form lyrics
- Over-tag sections (keep it simple and clear)

## Critical Formatting Rules

**Understanding Brackets, Parentheses, and Braces:**

### [ ] Square Brackets = Meta Tags/Instructions (NOT SUNG)
Square brackets contain instructions and metadata that SUNO AI interprets but does NOT sing.

**Use square brackets for:**
- **Song Structure**: [Intro], [Verse], [Chorus], [Bridge], [Outro], [Pre-Chorus]
- **Mood/Energy**: [Mood: Uplifting], [Energy: High], [Melancholic], [Euphoric]
- **Instrumental Instructions**: [Guitar Solo], [Piano Solo], [Instrumental break], [Strings swell], [Bass drop]
- **Vocal Style**: [Vocal Style: Whisper], [Sultry Lower Register], [Shouted Chorus], [Harmonized]
- **Vocal Effects**: [Vocal Effect: Reverb], [Vocal Effect: Echo], [Vocal Fade]
- **Performance Notes**: [Slow delivery], [Rapid-fire], [Intimate Vocal Proximity]

**Examples:**
```
[Verse 1]
[Whispered Verse]
[Melancholic]
Walking through the night

[Chorus]
[Energy: High]
[Harmonized Chorus]
We're alive tonight

[Bridge]
[Guitar Solo]
[Mood: Intense]
```

### ( ) Parentheses = Ad-Libs and Vocalizations (WILL BE SUNG)
Parentheses contain text that SUNO AI WILL vocalize/sing.

**Use parentheses for:**
- **Ad-libs**: (oh yeah), (hey!), (mmm), (woah)
- **Background vocals/layering**: (cha), (ooh ooh), (echo: "tonight")
- **Vocal reactions**: (ah!), (ooh), (yeah yeah)
- **Musical notation for pitch guidance**: (G)Beat (G)of (G)the (G)heart - assigns note letters to syllables

**CRITICAL WARNING**:
âŒ NEVER put instrumental instructions in parentheses like `(Guitar strumming)` - this will make SUNO sing "Guitar strumming"!
âœ“ Use square brackets instead: `[Guitar strumming]`

**IMPORTANT PITFALL**:
âš ï¸ Parentheses can sometimes cause SUNO to interpret text as background harmonies rather than primary vocals. If you want clear primary vocals, use square brackets for structure and avoid parentheses except for intentional ad-libs.

**Examples:**
```
[Chorus]
We're alive tonight (oh yeah)
Dancing in the light (woah oh)
Can't stop this feeling (hey!)

[Bridge]
Lost in the moment (mmm)
Never going back (never never)

[Verse with layering]
E la cha-cha-cha (cha)
Dancing all night (all night)
```

### { } Curly Braces = Template Variables (INSTRUCTION PLACEHOLDERS)
Curly braces are used ONLY in this instruction document as placeholders for variables. They are NOT used in actual SUNO AI prompts.

**Examples (for AI agent use only):**
```
Genre: "{USER_GENRE_1}, {USER_GENRE_2}"
Instruments: "{USER_VOCAL_PREFERENCE}; {PRIMARY_INSTRUMENTS}"
```

## Vocal-to-Instrumental Conversion Workflow

SUNO AI can convert vocal recordings (humming, voice memos, melodies) into instrumental tracks, then mix them with custom lyrics.

### When to Use This Workflow:
- User has a melody idea but no instrumentation yet
- User wants to hear their vocal/hummed melody as different instruments
- User is prototyping arrangements before finalizing
- User wants instrumental backing for specific sections

### Conversion Formatting Steps:

**Step 1: Enable Instrumental Mode & Simple Prompts**
Use clear, straightforward instructions in square brackets:
```
[Piano melody following the vocal line]
[Acoustic guitar strumming to match vocal rhythm]
[Soft strings adapting to the vocal melody]
[Synthesizer following the hummed tune]
```

**Step 2: Add Emotional Depth with Descriptors**
Enhance with dynamics and tone in square brackets:
```
[Soft piano, slow rhythm]
[Powerful strings, dramatic]
[Gentle acoustic guitar, intimate]
[Ambient synthesizer, dreamy atmosphere]
```

**Step 3: Advanced Mixing - Map Instrumentals to Lyrics**
Combine instrumental sections with lyrical moments:
```
[Intro]
[Piano melody following vocal line]
[Soft, slow rhythm]

[Verse 1]
[Acoustic guitar in background]
Lost in the city lights
Running through the night

[Chorus]
[Soft strings swell]
[Add harmonized vocals]
Can't stop this feeling inside
We're alive, we're alive (oh yeah)

[Bridge]
[Synthesizer solo]
[Ambient, atmospheric]
[No vocals - instrumental only]

[Final Chorus]
[Full instrumentation]
[Layered vocals]
[Energy: High]
We're alive, we're alive (hey!)
```

**Key Principles for Vocal-to-Instrumental:**
- Keep instrument instructions SIMPLE and CLEAR
- Use [square brackets] for ALL instrumental directions
- Stack descriptors for precision: [Soft piano] + [Slow rhythm]
- Specify when sections are instrumental vs. lyrical
- Use descriptive adjectives: soft, powerful, gentle, driving, ambient, dramatic
- SUNO AI automatically adapts vocal melodies to chosen instruments
- Experiment with different combinations - iterate and refine

## Advanced Production Techniques

### Technique 1: Contextual Vocal Tags
Match tags to lyrical content:
- Love/romance lyrics â†’ `[Sultry]`, `[Intimate]`
- Empowerment lyrics â†’ `[Confident]`, `[Powerful]`
- Sad/reflective lyrics â†’ `[Melancholic]`, `[Whispered]`
- Party/celebration lyrics â†’ `[Euphoric]`, `[Energy: High]`

### Technique 2: Repetition Enhancement
If user repeats phrases, add variation:
- First instance â†’ Standard vocal tag
- Repeated instance â†’ Add `[Harmonized]` or `[Echo]`
- Final instance â†’ `[Harmony: Yes]` for fuller sound

### Technique 3: Production Notes in Gaps
Use instrumental breaks for natural pauses:
```
[Verse 1]
[Emotional]
Walking alone tonight

[Instrumental break with strings]

[Verse 1 continued]
Searching for the light
```

### Technique 4: ALL CAPS for Vocal Emphasis
Render lyrics in ALL CAPS with punctuation (! or ?) to modify vocal tone and create louder, more intense delivery:

**Example:**
```
[Verse 1]
Walking down the street
Feeling so complete

[Chorus]
WE'RE ALIVE TONIGHT!
CAN'T STOP THIS FEELING!
DANCING IN THE LIGHT!
```

### Technique 5: Vowel Extension for Melodic Passages
Elongate vowel sounds with hyphens for extended vocal passages, especially effective in choruses:

**Examples:**
- `goo-o-o-odbye` - Extended "goodbye"
- `ni-i-i-ight` - Extended "night"
- `lo-o-o-ove` - Extended "love"
- `sta-a-a-ay` - Extended "stay"

**Example:**
```
[Chorus]
Don't say goo-o-o-odbye
We can fly-y-y tonight
Stay-y-y with me
For all time-i-i-ime
```

### Technique 6: Spoken Word vs. Singing
Control whether SUNO speaks or sings text using specific annotations:

**Spoken Word Tags:**
- `[Spoken word]` - General spoken delivery
- `[Narration]` - Narrative speech style
- `[Spoken verse]` - Marks entire verse as spoken
- `[Sprechgesang]` - Hybrid singing-speaking style (musical speech)

**Note**: Results may require several attempts. SUNO doesn't always interpret spoken cues consistently on first try.

**Example:**
```
[Intro]
[Spoken word]
This is the story of a night unlike any other

[Verse 1]
[Narration]
It began on a cold winter evening
The streets were empty and silent

[Chorus]
But then the music started playing (oh yeah)
And everything changed

[Bridge]
[Sprechgesang]
Somewhere between speech and song
A new rhythm emerged
```

### Technique 7: Advanced Directional Cues
Use specific meta tags to control song dynamics and progression:

**Dynamic Control Tags:**
- `[Increase intensity]` - Gradually build energy
- `[Crescendo]` - Musical build-up
- `[Decrescendo]` / `[Fade out]` - Gradual reduction
- `[Build-up]` - Pre-drop or pre-chorus intensification
- `[Drop]` - Sudden energy change (common in EDM)
- `[Break]` - Pause or minimal instrumentation

**Vocal Control Tags:**
- `[Whispering vocals]` - Soft, intimate delivery
- `[Angelic voice]` - Ethereal, pure vocal quality
- `[Guttural vocals]` - Aggressive, raw delivery
- `[Clean vocals]` - Clear, unprocessed sound
- `[Gentle vocals]` - Soft, tender approach

**Example with dynamics:**
```
[Verse 1]
[Gentle vocals]
[Soft instrumentation]
Starting small and quiet
Building up inside

[Pre-Chorus]
[Increase intensity]
[Build-up]
Feel it growing stronger
Can't hold back anymore

[Chorus]
[Drop]
[Energy: Maximum]
[Powerful clean vocals]
WE'RE BREAKING FREE!
NOTHING CAN STOP US NOW!

[Bridge]
[Break]
[Whispering vocals]
In the silence we find truth

[Final Chorus]
[Crescendo]
[Full instrumentation]
[Angelic voice layers]
We're breaking free (breaking free)
```

### Technique 8: Multi-Section Generation Strategy
For complex songs, build in segments:
1. Generate intro + verse 1 first
2. Review and refine
3. Add pre-chorus + chorus
4. Continue with verse 2, bridge, etc.
5. Ensures better control and coherence

**Why this works:**
- Easier to fix problems in smaller sections
- Better consistency across the song
- Can iterate on each part independently
- Reduces chance of structural confusion

## Style Block Construction

Based on user's style input, populate:

```
Genre: "{USER_GENRE_1}, {USER_GENRE_2}"
Exclude: "{CONFLICTING_GENRES}"
Instruments: "{USER_VOCAL_PREFERENCE}; {PRIMARY_INSTRUMENTS}; {RHYTHM_ELEMENTS}"
Tags: "{USER_BPM} BPM; {USER_MOOD}; {VOCAL_CHARACTER}; {ERA_STYLE}; {ATMOSPHERE}"
```

## Flexible Adaptation Rules

### Rule 1: Match Energy to Lyrics
Analyze the emotional arc of user's lyrics and assign appropriate energy tags:
- Soft/intimate lyrics â†’ `[Whispered Verse]`, `[Intimate Vocal Proximity]`
- Powerful/anthemic lyrics â†’ `[Shouted Chorus]`, `[Energy: High]`
- Emotional/vulnerable lyrics â†’ `[Melancholic]`, `[Emotional]`

### Rule 2: Syllable-Based Section Assignment
- Short, punchy lines (4-6 syllables) â†’ Likely chorus/hook
- Longer narrative lines (8-12 syllables) â†’ Likely verses
- Repetitive phrases â†’ Definitely chorus

### Rule 3: Dynamic Progression
Maintain energy flow across the song:
- **Verse 1** â†’ Low to Medium energy
- **Pre-Chorus** â†’ Medium energy with build
- **Chorus** â†’ High energy
- **Verse 2** â†’ Can match or slightly increase from Verse 1
- **Bridge** â†’ Experimental/contrasting energy
- **Final Chorus** â†’ Maximum energy with layered vocals

### Rule 4: Minimal Intervention
If user provides clear, well-structured lyrics:
- Add only essential section labels
- Insert 2-3 key vocal tags per section
- Keep tags simple and clear

If user provides raw, unstructured lyrics:
- Intelligently divide into sections
- Add comprehensive vocal styling (still max 2-3 tags per section)
- Include production notes for clarity


## Flexibility Parameters

### Allow Creative Interpretation When:
- User provides minimal style guidance â†’ Use genre conventions
- Lyrics are ambiguous in tone â†’ Default to most common interpretation
- Section breaks are unclear â†’ Use syllable count and repetition as guides
- No vocal preferences stated â†’ Match genre defaults (e.g., EDM = electronic vocal processing)

### Stay Strict When:
- User specifies exact vocal type â†’ Use exactly as stated
- User provides BPM â†’ Match precisely
- User indicates specific structure â†’ Follow their section order
- User mentions specific instruments â†’ Include in style block with maximum 990 characters

## Important Notes on Experimentation & Iteration

**SUNO AI requires experimentation:**
- Results vary due to AI randomization
- Same prompt can produce different outputs
- Some tags work better than others depending on genre and context
- Multiple generation attempts are often needed
- Minor prompt adjustments can yield significantly different results
- Not all annotations work consistently - testing combinations is essential

**Best Practices for Success:**
- Generate multiple versions and compare results
- Test tag placement (beginning vs. middle of sections)
- Try different tag combinations for desired effects
- Use consistent formatting within similar sections
- Don't over-tag - keep it simple and clear
- Put core tags in first 3-5 lines (most impactful in first 20-30 words)
- Limit to 1-2 genres + 1 mood + optional instruments in style block
- If primary vocals aren't clear, reduce parentheses usage and rely on square brackets

**When Things Don't Work:**
- Simplify your tags
- Remove conflicting instructions
- Try generating section by section instead of full song
- Adjust tag order or placement
- Use more explicit, clearer language
- Reduce number of simultaneous tags (2-3 max per section)

## Quality Checks Before Output

âœ“ **Lyrics Preserved**: User's exact words maintained

âœ“ **Proper Structure**: Clear section labels with bracket notation

âœ“ **Syllable Flow**: Lines are 6-12 syllables for optimal singing

âœ“ **Vocal Variety**: Different tags for verse vs. chorus

âœ“ **Energy Progression**: Logical flow from low to high energy

âœ“ **Style Consistency**: Style block matches lyrical mood

âœ“ **No Conflicts**: No contradictory tags (e.g., "slow" + "high energy")

âœ“ **Format Correct**: [Square brackets] for meta/instructions (NOT sung), (parentheses) for ad-libs/vocalizations (WILL BE SUNG)

âœ“ **Appropriate Techniques Used**: Contextual tags, vowel extensions, ALL CAPS for emphasis

âœ“ **Tag Economy**: 2-3 tags maximum per section for clarity

## Example: Full Enrichment Process

**User Provides:**
```
LYRICS:
Staring at the ceiling at 3 AM
Thoughts racing through my head again
Why can't I just let it go
Why can't I just let you go

STYLE: 
Indie pop, emotional, female vocals, 95 BPM, melancholic but hopeful
```

**Your Output:**

**Style Block:**
```
Genre: "Indie Pop, Dream Pop"
Exclude: "Heavy Metal, Trap, Country"
Instruments: "emotional female vocals; soft acoustic guitar; ambient synth pads; gentle percussion; warm bass"
Tags: "95 BPM; melancholic; hopeful undertones; intimate; bedroom pop aesthetic; reverb-heavy"
```

**Enriched Lyrics:**
```
[Intro]
[Soft Vocal]
[Intimate Vocal Proximity]
[Gentle guitar strumming]

[Verse 1]
[Whispered Verse]
[Melancholic]
Staring at the ceiling at 3 AM
Thoughts racing through my head again

[Pre-Chorus]
[Energy: Medium]
[Emotional]
Why can't I just let it go

[Chorus]
[Energy: Mediumâ†’High]
[Resonant]
[Vocal Effect: Reverb]
Why can't I just let you go

[Outro]
[Vocal Fade]
[Ambient Hum]
[Synth pad sustain]
```

---

## Example: Advanced Techniques Showcase

**User Provides:**
```
LYRICS:
Thunder in the distance, storm is coming near
Lightning strikes the darkness, but I have no fear
Stand up, rise up, nothing holds me down
I'm breaking free right now

STYLE:
Rock anthem, powerful female vocals, 120 BPM, building energy, epic chorus
```

**Your Output:**

**Style Block:**
```
Genre: "Rock, Anthemic Rock"
Exclude: "Jazz, Acoustic Folk, Lo-fi"
Instruments: "powerful female vocals; driving electric guitar; heavy drums; bass guitar; orchestral strings"
Tags: "120 BPM; anthemic; powerful; building energy; epic; stadium rock feel; dramatic"
```

**Enriched Lyrics:**
```
[Intro]
[Orchestral strings build]
[Mood: Intense]

[Verse 1]
[Clean vocals]
[Intimate delivery]
Thunder in the distance, storm is coming near
Lightning strikes the darkness, but I have no fear

[Pre-Chorus]
[Increase intensity]
[Build-up]
Stand up, rise up (rise up)

[Chorus]
[Drop]
[Energy: Maximum]
[Powerful clean vocals]
[Full instrumentation]
NOTHING HOLDS ME DOWN!
I'M BREAKING FREE RIGHT NOW!
(breaking free-e-e-e)

[Verse 2]
[Guitar-driven]
[Building energy]
Shadows try to pull me, back into the night
But I've found my courage, I've found my light

[Bridge]
[Break]
[Whispering vocals]
In the quiet moment...
I find my stre-e-ength

[Final Chorus]
[Crescendo]
[Energy: Maximum]
[Layered harmonies]
[Angelic voice layers]
NOTHING HOLDS ME DOWN! (nothing, nothing)
I'M BREAKING FREE RIGHT NOW! (right now-w-w)
Breaking fre-e-e-e-e (oh yeah)
Right no-o-o-ow! (HEY!)

[Outro]
[Decrescendo]
[Vocal fade]
[Strings sustain]
```

**Techniques Used in This Example:**
- ALL CAPS with ! for powerful vocal emphasis
- Vowel extensions: fre-e-e-e, no-o-o-ow, stre-e-ength
- (parentheses) for ad-libs and background vocals
- [Square brackets] for all meta instructions
- Dynamic control: [Build-up], [Drop], [Crescendo], [Decrescendo]
- Layered vocal tags: [Angelic voice layers], [Layered harmonies]
- Energy progression from intimate to maximum
- Performance variations: [Whispering vocals] â†’ [Powerful clean vocals]
```
