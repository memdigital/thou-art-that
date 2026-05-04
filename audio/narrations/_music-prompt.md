# TAT background music: ElevenLabs Music API prompt

For use against `luma-elevenlabs/v1/music`. Worker forces `force_instrumental: true`.

## Prompt v1 (for testing)

```
A slow, contemplative lo-fi piece. 65 bpm. Warm Rhodes piano with soft
analog pad underneath, vinyl texture audible but understated. Minimal
melodic movement, long held notes, gentle harmonic shifts every eight
bars. No drums or percussion. The mood is meditative warmth, like a
candle in a wood-panelled room. Suitable to loop quietly under
philosophical narration. Instrumental.
```

## Why these choices

- **65 bpm**: slow enough to underpin contemplative narration without competing for attention
- **Rhodes + pad**: warm, no plucky/bright tones that fight Nura's voice
- **No drums**: drumless lo-fi is rarer but cleaner under spoken word; brushed drums optional v2 if v1 feels lifeless
- **Vinyl texture understated**: atmosphere, not pastiche
- **8-bar harmonic shifts**: gives shape without distracting
- **"Wood-panelled room" cue**: pulls the ElevenLabs prior toward intimate, not study-cafe

## Mix discipline (post-generation)

- Voice (Nura): -16 LUFS integrated
- Music bed: **-24 LUFS integrated** (heavily under, ambient presence not foreground)
- Stinger (canonical Marbl, 9s): -16 LUFS, prepended cleanly with no bed underneath
- Crossfade bed in over 1.5s after stinger ends so it sneaks in
- Crossfade bed out over 2s at track end

## Integration sequence (per track)

1. Generate voice MP3 via `/tts {voice: 'nura-tat', text: <paced script>}`
2. Note voice duration (D)
3. Generate music bed via `/music {prompt: <above>, durationSeconds: D + 4}` (extra for fade in/out)
4. ffmpeg mix: stinger + (voice over bed) + tail-fade
5. Output stereo 44.1kHz, 128kbps (matches existing audio pipeline)
