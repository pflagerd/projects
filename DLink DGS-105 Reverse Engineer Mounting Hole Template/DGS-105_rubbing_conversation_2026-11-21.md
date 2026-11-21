# D-Link DGS-105 mounting-slot rubbing: conversation excerpt

Saturday, November 21, 2026. Verbatim excerpt, starting at the rubbing question. Exchanges about other topics are left out.

---

**Daniel:** I've taken a rubbing of the temp of the back of that D link and it shows up the outlines quite nicely. Uh, I'm presuming if I scanned this, then I could probably feed it into some kind of OCR reader or something that might be able to come up with a like a scaled vector graphic of it. Is that true?

**Claude:** Yes, more or less, though the term is tracing or vectorizing, not OCR, which is just for text. Without looking it up: Inkscape, which is open source, has a Trace Bitmap feature that turns a scan into SVG paths, built on a tool called potrace.

Two tips. Scan at a known resolution, say 600 dpi, and lay a ruler in the scan so you can verify the scale. And a pencil rubbing is grainy, so expect to clean up the outline a bit.

Want me to find the official Inkscape docs for that?

**Daniel:** Yeah, please.

**Claude:** Sure, looking that up now.

Found it, and it confirms what I said. Inkscape's own tutorial has you import the scan, select it, then open Trace Bitmap from the Path menu, or press Shift+Alt+B. The beginners' guide adds that a dialog opens with options and an Update button for refreshing the preview as you tweak them.

[The official tracing tutorial](https://inkscape.org/doc/tutorials/tracing/tutorial-tracing.html) is in the chat. For a pencil rubbing, I'm guessing the brightness cutoff mode will suit best, but that's my hunch, not from the docs.

**Daniel:** Okay, not familiar with that, but we can get there.

**Claude:** No bother, it's simpler than it sounds. When you've got the scan up on the 7750, give me a shout and I'll walk you through it one step at a time.

---

**Daniel:** Just about to use the scanner to scan that D-Link rubbing.

**Claude:** Good timing. Two things before you hit scan: set the resolution to something known, like 600 dpi, and lay a ruler alongside the rubbing so we can check the scale afterwards. I'd also save it as PNG, not JPEG, so the edges stay crisp for tracing.

**Daniel:** Man, the HP and Windows software suck. They are so bad.

**Claude:** Ugh, they really are a slog. You could skip them: I believe Kubuntu ships with a scanning app, Skanpage or Skanlite, and I'm guessing it'll see the HP over the network without extra drivers, though I haven't verified that for your model.

Want to try it from the 7750 instead?

**Daniel:** No, I'll keep that in mind for next time, but right now I'm gonna go ahead.

**Claude:** Fair enough. One small thing while you're in there: save it as PNG or TIFF if it offers, since JPEG smears the fine edges a bit. Shout when you've got the file.

**Daniel:** Why wouldn't I save it as a JPEG instead of a PDF?

**Claude:** Between those two, JPEG is the better pick. A scanned PDF is just a wrapper around an image, often a JPEG anyway, so it adds an import step in Inkscape for no gain.

And honestly, at 600 dpi and high quality, a JPEG will trace fine. PNG is just a touch cleaner because it's lossless.

**Daniel:** and I've got none compression.

**Claude:** Perfect, go with none. That gives you the cleanest edges for tracing, and the bigger file size won't matter for one page.

**Daniel:** what model did I read you before on that D-Link?

**Claude:** The D-Link DGS-105, the 5-port gigabit switch.

---

**Daniel:** Looks like Inkscape site is down at the moment anyway. I tried a few different ways of tracing the bitmap and they all produce terrible results.
I wonder, is this the kind of thing you might be able to do?

**Claude:** Quite possibly, yes. If you drop the scan into this chat, I can run image processing on it and try to pull out the slot outlines as an SVG at true scale, as long as I know the scan resolution. No promises until I see how grainy the rubbing is.

Honestly, though, all you really need is the centre-to-centre distance between the two slots, and that I could measure from the scan far more reliably than a full trace.

Want to upload it and I'll have a go?

**Daniel:** Yeah, I'll do that. I'm going to upload it in a different window than the one I'm using, but I think this should work.

**Claude:** Should do, as long as it's this same conversation open in the other window; if it lands in a new chat, I won't see it from here. Tell me once it's up, and what resolution you scanned at.

**Daniel:** *(uploaded the scan: `Dlink_DGS105_Mounting_Hole_Rubbing_2026-11-21_112531.jpg`)*

**Claude:** The scan came through; I'll measure the slot spacing from it and try to pull out the outlines.

The slots come out at about **58 mm centre to centre** (2.29 in), but that number rests on one assumption about the scan's scale, so check it with a ruler before drilling.

- **Scale assumption:** the file I received is 1870 × 2576 px with no resolution recorded in it. That shape matches a full 8.5 × 11.7 in scanner glass, which works out to 220 px per inch. I'm guessing the upload was downsized from your original scan; if the scan didn't cover the full 8.5 in width, the 58 mm is wrong in proportion.
- **Measurement itself:** the offset between the two slots is 503 px, found by matching the left outline onto the right one. It was stable to within a pixel or two (about ±0.25 mm), plus whatever the paper shifted while you rubbed.
- **Slot shape:** these aren't simple keyholes. Each is a double-ended slot about 19 mm long, roughly 9 mm wide in the middle and 4.6 mm wide at each end. I'm theorizing the screw head enters at the wide middle and slides to either end, about 7 mm from centre.
- **Screw size:** on those numbers the head needs to be under about 8.5 mm across with a shank under about 4.5 mm. One of the 3D-printed mount listings from earlier mentioned #6 screws, which would fit, but that's a hobbyist's note, not D-Link's spec.

`DGS-105_mount_template.svg` is drawn in millimetres with an idealized slot outline (not a literal trace of the grainy rubbing), crosshairs at both centres, and a 50 mm check bar. Print it at 100% and measure the bar; if it isn't 50 mm, the printer scaled it. `DGS-105_slot_measurement_check.png` shows the fitted outlines laid over your rubbing so you can judge the match yourself.

The two holes sit on a line perpendicular to the slots, so mark them level, 58 mm apart.

What resolution did you scan at, and what are the pixel dimensions of the original file? If it's 2550 px wide at 300 dpi (or 5100 at 600), the scale assumption is confirmed.

---

*The following exchange was by voice, while the scan was being processed in the desktop window.*

**Daniel:** Six hundred DPI, and it's a little bit kilter, a kilter.

**Claude:** Got it, 600 dpi, and a bit of skew is no problem, since the distance between the two slots comes out the same whichever way the page is turned. Let me see if the file's come through.

Nothing's reached me yet, the upload folder on my side is empty. It may still be sending, or it's gone into a different chat. Does the other window show it as attached in this same conversation?

**Daniel:** Does.

**Claude:** Right, let me look again.

Still nothing on my side, I'm afraid. Two guesses: an attachment only reaches me once the message is actually sent, not just attached, or the file's too big, since an uncompressed full page at 600 dpi could be around 100 MB.

Has the message been sent, or is it still sitting in the box?

**Daniel:** This is about 1.2 megabyte. It looks like the other instance is working on it.

**Claude:** Ahh, then it went to the text side, and that's fine, let it do the job. I can't see the file or its answer from here, so make sure it knows the scan is 600 dpi, and ask it for the centre-to-centre distance between the two slots.

Read me what it comes back with and I'll sanity-check it.

**Daniel:** Oh, I see why. I think that's actually a Claude code.

**Claude:** That'd explain it. Claude Code is a separate session from this one, so I never saw the file. No harm done, though: it's got the scan right there on disk, so it's well placed to do the measuring. Same ask applies, 600 dpi and the centre-to-centre distance between the slots.

**Daniel:** Desktop window.

**Claude:** Right, that's a separate session from this call, so it never comes to me. No harm done, it's well suited to the job since it has the file right there. Just give it the 600 dpi figure and ask for the slot spacing, and I'll sanity-check the number.

**Daniel:** Well, I, I mean, I could see our conversation in real time uh, I had it on the chat selection of the desktop.

**Claude:** Hmm, then it is this conversation, and I'd expect to see it. Let me check once more.

I've looked three times now and the file still isn't anywhere on my side, even though it's the same conversation. I don't know why; my guess is an attachment sent from the desktop window gets handled by the text side and isn't passed to me on the call.

So let the desktop side do the measuring. Has it come back with a number yet?

**Daniel:** No, it's uh, taken a minute. It's trying quite a few things.

**Claude:** No rush, a grainy rubbing takes some coaxing. If it gets bogged down, there's a low-tech fallback: measure centre to centre straight off the rubbing with a ruler or calipers, and that's your number.

**Daniel:** Holy cow, it's finished and it's produced something absolutely fantastic.

**Claude:** Brilliant, that's great news! I can't see it from here, so what did it give you: an SVG outline, and did it come up with a centre-to-centre distance for the slots?

**Daniel:** It did, 58.1 millimeters.

**Claude:** That's plausible. From memory the switch body is about 100 mm wide, so 58.1 mm between slots fits comfortably, though I've no official figure to check it against. It's about 2.29 inches.

Before you drill, I'd hold a ruler across the actual slots as a quick cross-check, since a slightly off scan scale would shift that number.

**Daniel:** Gosh, you know, he, he, Claude instances and other AIs at this level of sophistication are going to obsolete a lot of hand work in things like Inkscape.

**Claude:** I think you're right for the tedious end of it: tracing, cleanup, converting one format to another. What I'd guess sticks around is the judgement part, knowing what the drawing is for and catching it when the output looks right but is a millimetre off, which is why I keep nagging you about that ruler.

**Daniel:** Yeah. Good point.

**Claude:** Cheers. Go and get that switch on the wall, then, and shout if the holes don't line up.
