# Image assets

Suggested destination folder path:
/Volumes/Thinker/Thinker/HarmoniXHR/Website/Repos/hxhr-sites/assets/img/

## Provenance

On 2026-08-28 index.html was decoupled from the GoHighLevel CDN. All nine
images it referenced were downloaded from the GHL asset account
`x48r2jr2UDphtVIF0xua` on `assets.cdn.filesafe.space` and relocated into this
directory, and the nine references in index.html were rewritten to local
relative paths.

At the time of the relocation the GHL account was still live and serving every
one of the nine files: each returned HTTP 200 when fetched. The relocation was
done to remove the dependency, not in response to any loss of access. Nothing
here should be read as a record that the GHL account has been deleted or has
stopped serving these files.

Eight of the nine were copied byte for byte, verified by md5 at both ends. The
logo is the one exception and is held as two files, described below.

## The logo, two files

- `logo-original.png` is the unmodified master as downloaded, 5331x1945,
  754445 bytes, md5 9b12f1ab6e9b8fee05f3d9849cced3ca. It is archival. Nothing
  in index.html points at it.
- `logo.png` is the served derivative, resampled to 600px wide (600x219),
  39203 bytes. The alpha channel is preserved: both files are PNG colour
  type 6, truecolour with alpha. This is the file index.html references.

The original is retained because the derivative is lossy in resolution and
cannot be enlarged back. Anything needing print resolution or a different
served size should be generated from `logo-original.png`, not from `logo.png`.

## Mapping, local filename to original CDN filename

All CDN paths were under:
https://assets.cdn.filesafe.space/x48r2jr2UDphtVIF0xua/media/

| Local file | Original CDN filename | md5 | Used by |
|---|---|---|---|
| logo.png | 6a920c34722007d7ff16315d.png (resampled) | derivative, not byte-identical | nav logo, index.html L180 |
| logo-original.png | 6a920c34722007d7ff16315d.png | 9b12f1ab6e9b8fee05f3d9849cced3ca | archival, unreferenced |
| hero-background.jpg | 6a91f4ce0914f11215f65f4e.jpg | 1985a637bf6eb2742930085c02af92c9 | CSS .hero-bg, index.html L47 |
| clifford-der.jpg | 6a91f3120914f11215f63a72.jpg | 1659be6bf050261cc6a70fae65c21d9a | portrait, index.html L375 |
| meritain-health.jpg | 6a91f311934a62aec86c00f5.jpg | cb5b03f767c7df49eb36f506ab939164 | carrier logo, index.html L397 |
| brms-east-west-administrators.jpg | 6a91f3114fe741935436fffb.jpg | bea00cc7e72b4abc816b9f514c0552c8 | carrier logo, index.html L398 |
| kaiser-permanente.jpg | 6a91f311854f9696b3bed606.jpg | 69cbb4a85f93e7eca978132ebcd3ba6f | carrier logo, index.html L399 |
| unitedhealthcare.jpg | 6a91f3114fe741935436ffff.jpg | 75df86bc64ae3a739f02c08ef9cefef0 | carrier logo, index.html L400 |
| anthem-blue-cross-blue-shield.jpg | 6a91f31148ca8386eb04667b.jpg | 5df33a3796fec9996d02851952f768f7 | carrier logo, index.html L401 |
| cigna.jpg | 6a91f3110914f11215f63a44.jpg | b65ebab38fbbd794f21a8d04409815a6 | carrier logo, index.html L402 |

The CDN hashes are recorded so the mapping stays recoverable: the local names
were derived from each image's alt text, which is not something the CDN
filenames encode.

Two of the source hashes differ by a single character
(`...436fffb.jpg` and `...436ffff.jpg`, BRMS and UnitedHealthcare). They are
different images, confirmed by md5. Take care if either is ever re-fetched
by hand.

## Note on the carrier marks

The carrier and administrator logos appear on the page under the disclaimer at
index.html L404: they identify appointments held by Clifford Der as a licensed
producer and do not imply endorsement, sponsorship or affiliation. Relocating
the files does not change that. They remain the property of their respective
owners.

Last updated: 2026-08-28
