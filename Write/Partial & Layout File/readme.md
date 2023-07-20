sch: https://www.google.com/search?q=flashrom+partial+write+layout+file, https://www.google.com/search?q=flashrom+Error%3A+Image+size+doesn%27t+match+the+expected+size

Discuss:
- https://flashrom.flashrom.narkive.com/74qFhzRd/image-size-doesn-t-match-the-flash-chip-s-size

Bug report
- https://github.com/flashrom/flashrom/issues/45


# Solution: 
sch: https://www.google.com/search?q=flashrom+padding

## DD method
works:
- https://plutiedev.com/rom-padding

example:
`cat original.bin /dev/zero | dd bs=1024 count=4096 of=padded.bin`

**worked for me:** for getting exact size!
`cat original.bin /dev/zero | dd bs=1 count=8388608 of=padded.bin`
