# SORA Video Generation Prompt - Salesforce Rescue Hero Video

## Primary Prompt for SORA

```
A professional 30-second founder introduction video filmed in a modern home office. 

A confident, approachable man in his 30s-40s with a casual professional appearance (button-down shirt or polo) sits at a clean desk with a laptop and subtle tech equipment visible in the background. Natural window lighting illuminates his face from the side, creating a warm, trustworthy atmosphere. The background shows bookshelves with tech books and subtle Salesforce certifications or awards.

He looks directly at the camera with friendly, confident eye contact and speaks with genuine warmth and expertise. His body language is relaxed but professional - occasional hand gestures that feel natural, not scripted. The camera is positioned at eye level in a medium close-up shot, creating an intimate, conversational feel.

The overall aesthetic is authentic and human - NOT corporate, NOT AI-generated, NOT overly polished. Think "expert colleague helping you solve a problem" rather than "slick sales pitch." Subtle depth of field keeps focus on the speaker while the background provides context without distraction.

Lighting: Natural soft key light from window + subtle fill light to eliminate harsh shadows. Color temperature: Warm (3200K-4000K). 

Camera: Steady, locked-off shot. No camera movement. 16:9 aspect ratio, 1080p resolution. Professional but approachable production quality.

Duration: 30 seconds of steady, confident presentation.
```

## Alternative Simplified Prompt

```
Professional home office setting. Man in business casual attire (button-down shirt) sitting at desk speaking directly to camera. Natural window lighting, warm tones. Modern but not corporate. Bookshelves with tech books visible in background. Medium close-up shot, eye-level camera angle. Confident, friendly demeanor. Real human, not AI-generated. 30 seconds, 16:9, 1080p.
```

## Visual Style References

**Tone Keywords for SORA:**
- Authentic
- Approachable
- Professional but casual
- Warm lighting
- Natural setting
- Tech-savvy but human
- Trustworthy
- Expert consultant
- Not corporate/stiff
- Not AI/synthetic

## Technical Specifications

- **Duration**: 30 seconds minimum, up to 60 seconds maximum
- **Aspect Ratio**: 16:9 (horizontal)
- **Resolution**: 1920x1080 (1080p) or 1280x720 (720p minimum)
- **Frame Rate**: 24fps or 30fps
- **Format**: MP4 (H.264 codec)
- **Audio**: Can be silent (voiceover will be added) or ambient office sounds

## Scene Description for SORA

**Setting**: Modern home office
- Clean, organized desk
- Laptop (MacBook preferred) open but screen not visible
- 1-2 tech books on desk edge
- Background: Bookshelf with business/tech books
- Subtle certification frames or awards (not prominent)
- Window with natural light (blurred in background)
- Neutral wall color (white, light gray, or warm beige)

**Subject**: Professional male founder
- Age appearance: 30s-40s
- Casual professional attire: Button-down shirt (blue, white, or gray) or quality polo
- Well-groomed, professional haircut
- Clean-shaven or neat beard
- Friendly, approachable demeanor
- Confident but not arrogant
- Genuine smile that reaches the eyes
- Direct eye contact with camera

**Lighting**:
- Primary: Natural window light from left or right (soft, diffused)
- Fill: Subtle indoor lighting to balance shadows
- No harsh overhead lights
- Warm color temperature (looks like afternoon)
- Face well-lit, no dark shadows under eyes

**Camera Work**:
- Static camera (no movement, no zooms)
- Eye-level angle (not looking down or up at subject)
- Medium close-up: Head, shoulders, and upper chest visible
- Subject centered or slightly off-center (rule of thirds)
- Shallow depth of field: Subject sharp, background slightly blurred

## What to Avoid (SORA Negative Prompts)

❌ Corporate boardroom setting
❌ Suit and tie (too formal)
❌ Dark, dramatic lighting
❌ Stock photo aesthetic
❌ Overly polished/sterile environment
❌ Generic office cubicle
❌ Artificial/synthetic look
❌ Webcam-quality low production
❌ Fish-eye or unusual camera angles
❌ Busy, cluttered background
❌ Fluorescent lighting
❌ Green screen artificial background

## Post-Generation Checklist

After SORA generates the video:
- [ ] Subject appears trustworthy and professional
- [ ] Lighting is warm and natural (not harsh)
- [ ] Background is visible but not distracting
- [ ] Eye-level camera angle maintained
- [ ] No AI artifacts or uncanny valley effects
- [ ] 16:9 aspect ratio correct
- [ ] Duration 30-60 seconds
- [ ] Quality sufficient for web (1080p or 720p minimum)

## Voiceover Script (Add in Post-Production)

```
Hey, I'm Tyler. I founded Salesforce Rescue. 

I've been working with Salesforce for over 15 years, with deep expertise in emergency scenarios and complex technical architecture.

I have a track record of helping companies — both small and large — solve urgent Salesforce problems extremely quickly.

Whether you're dealing with data loss, automation failures, integration issues, or you're not even sure what's wrong... I'd love to help you get back on track.

This is a real conversation, not AI. Let's talk.
```

**Timing**: ~45-50 seconds when delivered naturally

## Alternative: If SORA Can't Generate People Reliably

**Plan B - Abstract/Motion Graphics Prompt:**

```
Professional animated text introduction on clean white background with subtle gradient. 

Text appears smoothly, one line at a time:
"Salesforce Rescue"
"15+ Years of Emergency Response Expertise"
"Senior-level Salesforce Architecture"
"Real Human Support, Not AI"
"When Salesforce Breaks... We Fix It Fast"

Minimal animation: Fade in, scale slightly. Color: Deep red (#dc2626) for emphasis words. Professional sans-serif font (Inter or similar). 30 seconds duration. Clean, modern aesthetic. Not flashy - confident and authoritative.
```

## File Naming Convention

Once generated, save as:
- `salesforce-rescue-hero-video-v1.mp4` (raw from SORA)
- `salesforce-rescue-hero-video-final.mp4` (with voiceover added)

## Integration Instructions

After video is ready:
1. Upload to `/Users/tyler/Salesforce Rescue/Website/` directory
2. Update `index.html` at lines 222-234
3. Replace placeholder div with:
   ```html
   <video controls poster="hero-video-poster.jpg" class="w-full rounded-2xl">
       <source src="salesforce-rescue-hero-video-final.mp4" type="video/mp4">
       Your browser does not support the video tag.
   </video>
   ```
4. Create poster image (thumbnail) from best frame of video

---

## Notes

- SORA works best with descriptive visual prompts rather than narrative scripts
- If generated person doesn't look like you, that's okay - the key is trustworthy, professional demeanor
- Can iterate on prompt to adjust lighting, setting, or subject appearance
- Video should feel like a Loom recording from an expert consultant, not a TV commercial
- Bob emphasized: "NOT AI-generated" - ironic, but the aesthetic should feel authentic and human
