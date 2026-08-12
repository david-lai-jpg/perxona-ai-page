# Lessons Learned

<!-- Genuinely useful discoveries for future sessions -->

- Perxona `presentationMode="embedded"` fills its parent but does not create height. Give the wrapper an explicit height; style the wrapper instead of `sv-agent`.
- Lazy-mount the Perxona custom element when the dialog first opens. This avoids loading its large avatar assets before a visitor asks to use it.
- The current Perxona bundle can request duplicate archive assets and return `ERR_ABORTED`; two optional motion `native.zip` assets also return `403`. Treat these as provider-side only after the profile, conversation, voice-token, avatar, and rendered-state checks all pass.
