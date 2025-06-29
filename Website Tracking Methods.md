## Browser & Device Fingerprinting
These identify users based on unique combinations of settings and hardware:
1. **[[User agent string]]** – Info about your browser, operating system, and version.  
2. **[[Screen resolution & color depth]]** – Size of your screen and how many colors it can show.  
3. **[[Timezone & system locale]]** – Your local time zone and language settings.  
4. **Installed fonts** – What fonts are installed on your device.  
5. **Installed plugins/extensions** – Some browser add-ons can be detected.  
6. **Audio fingerprint** – Unique audio output patterns from your device using sound tests.  
7. **Canvas fingerprinting** – How your browser draws graphics on an HTML5 canvas.  
8. **WebGL fingerprinting** – Graphics card details based on how 3D content is rendered.  
9. **Touch support** – Whether your device supports touch input.  
10. **Battery status API** – Info about your battery (level, charging status) on some devices.  
11. **Device memory and hardware concurrency** – Amount of RAM and number of processor threads.  
12. **Media device enumeration** – Names or types of connected cameras, microphones, etc.  
13. **Font smoothing and anti-aliasing** – How text is rendered/smoothed on your screen.
> These combined can uniquely identify you with >95% accuracy.
## Network & Connection Information
Websites can glean network characteristics from:
1. **IP address** – Can reveal your geo-location, ISP, and even specific device with IPv6.  
2. **TLS/SSL session identifiers** – Unique session IDs that can help track users across secure connections.  
3. **Connection speed and type** – Detected via the Network Information API (e.g., 4G, Wi-Fi, etc.).  
4. **Proxy/VPN detection** – Based on IP leaks, WebRTC, or unusual routing patterns.
## Storage Mechanisms
Persistent data storage in your browser:
1. **HTTP Cookies** – Small pieces of data stored by websites to track you across visits.  
2. **Local Storage / Session Storage** – Browser-based storage that can retain data even without cookies.  
3. **IndexedDB** – A more powerful browser storage option often used for persistent tracking.  
4. **Web SQL** – Deprecated but still functional in some browsers, used for storing data locally.  
5. **Flash cookies (LSOs)** – Older form of tracking that can persist even after clearing browser cookies.  
6. **ETags / Cache-based tracking** – Tracks users by checking unique cache identifiers set by the server.  
7. **Service Workers** – Background scripts that can continue running and tracking even when you’re not actively using the site.
## Behavioral Tracking
Tracks how you interact with a site:
1. **Mouse movements & scrolling behavior** – Tracks where and how you move your mouse or scroll the page.  
2. **Click/tap heatmaps** – Records where users click or tap most often on a page.  
3. **Keystroke timing patterns** – Measures how fast and in what rhythm you type, used for fingerprinting.  
4. **Interaction timestamps** – Logs the exact time of your actions (clicks, scrolls, keypresses, etc.).  
5. **Navigation patterns across sessions** – Tracks how you move between pages or sites over time.  
6. **Copy/paste or form-fill behavior** – Monitors text you copy/paste or autofill into forms.
> Often used in bot detection and user profiling.
## Cross-Site and 3rd-Party Tracking
Tracking across websites you don’t even visit directly:
1. **3rd-party cookies** – Cookies set by domains other than the one you're visiting, used for cross-site tracking.  
2. **Facebook Pixel, Google Analytics, etc.** – Tracking scripts that monitor user behavior across websites.  
3. **Content Delivery Networks (e.g., Cloudflare, Akamai)** – Can log requests and IPs to build user profiles.  
4. **Social media embeds (Like/Share buttons)** – Can track you even if you don’t interact with them.  
5. **Ad scripts and trackers** – Used by advertisers to build behavior profiles and retarget users.  
6. **Tracking pixels (1x1 images)** – Invisible images that load from a server to log your visit and actions.
## Link & URL-Based Tracking
Data passed in URLs or modified links:
1. **UTM parameters** – Tags in URLs used to track where traffic is coming from (e.g., newsletters, ads).  
2. **Affiliate codes** – Embedded in links to track referrals and assign credit for conversions.  
3. **Email open trackers** – Invisible images in emails that notify the sender when you open the message.  
4. **Click-tracking redirect links** – Links that route through tracking servers before taking you to the real destination.
## Advanced and Covert Techniques
More obscure or aggressive methods:
1. **CNAME cloaking** – Third-party trackers masquerade as first-party domains to bypass blockers.  
2. **HSTS supercookies** – Abuse of HTTP Strict Transport Security to store tracking data across sessions.  
3. **Browser history sniffing** – Attempts to detect your browsing history (mostly patched but still exploited in some ways).  
4. **Zombie cookies** – Cookies that come back after deletion by being regenerated from other storage areas.  
5. **WebRTC IP leaks** – Reveals your real IP address even when behind a VPN.  
6. **Fingerprint reshuffling detection** – Detects when you're trying to spoof or rotate your fingerprint, exposing anti-tracking efforts.
## Account or App-Based Identifiers
Once you're logged in, tracking gets easier:
1. **Email address** – Can be used to link activity across platforms and services.  
2. **Phone number** – Acts as a persistent identifier, often tied to identity and used for cross-device tracking.  
3. **Device IDs (on mobile apps)** – Unique identifiers (like IDFA on iOS or AAID on Android) used for tracking across apps.  
4. **OAuth token re-use** – Tokens issued for login can be reused or misused to identify and track users.  
5. **Login cookies or session tokens** – Persistent tokens that identify you after login, trackable across sites.  
6. **Single sign-on (SSO) providers like Google or Facebook** – Centralized login systems that can track your usage across every site you log into.