### injected.js
```javascript
// Spoof Timezone
const originalIntl = Intl.DateTimeFormat;
Intl.DateTimeFormat = function(...args) {
  const dtf = new originalIntl(...args);
  dtf.resolvedOptions = function() {
    return {
      timeZone: "UTC",
      locale: "en-US"
    };
  };
  return dtf;
};

// Spoof navigator.language
Object.defineProperty(navigator, 'language', {
  get: () => 'en-US'
});

// Spoof navigator.languages
Object.defineProperty(navigator, 'languages', {
  get: () => ['en-US', 'en']
});
```