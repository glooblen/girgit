### manifest.json
```json
"content_scripts": [
  {
    "matches": ["<all_urls>"],
    "js": ["content.js"],
    "run_at": "document_start"
  }
]
```
### content.js
```javascript
const script = document.createElement('script');
script.src = chrome.runtime.getURL('injected.js');
script.onload = () => script.remove();
(document.head || document.documentElement).appendChild(script);
```
### injected.js
```javascript
Object.defineProperty(screen, 'width', {
  get: () => 1920
});

Object.defineProperty(screen, 'height', {
  get: () => 1080
});

Object.defineProperty(screen, 'availWidth', {
  get: () => 1920
});

Object.defineProperty(screen, 'availHeight', {
  get: () => 1040
});

Object.defineProperty(screen, 'colorDepth', {
  get: () => 24
});

Object.defineProperty(screen, 'pixelDepth', {
  get: () => 24
});
```