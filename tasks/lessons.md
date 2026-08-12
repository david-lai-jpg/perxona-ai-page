# Lessons Learned

<!-- Genuinely useful discoveries for future sessions -->

- Perxona `presentationMode="embedded"` fills its parent but does not create height. Give the wrapper an explicit height; style the wrapper instead of `sv-agent`.
- Lazy-mount the Perxona custom element when the dialog first opens. This avoids loading its large avatar assets before a visitor asks to use it.
