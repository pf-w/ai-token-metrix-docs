# AI Token Metrix — Privacy Policy (HTML)

Ready-to-publish HTML version of the Privacy Policy for GitHub Pages hosting.

## Files

| File | Purpose |
|---|---|
| `index.html` | Landing page — bilingual language selector; auto-redirects Chinese browsers to `zh-Hans.html` on first visit |
| `en.html` | Full English version |
| `zh-Hans.html` | Full Simplified Chinese version |
| `style.css` | Shared styles (system font, light/dark auto, responsive) |

## Placeholders to replace before publishing

Search & replace across `en.html` and `zh-Hans.html`:

| Placeholder | Replace with |
|---|---|
| `[YOUR_NAME]` | Legal name / developer entity name (as registered with Apple) |
| `[SUPPORT_EMAIL]` | Support email address (e.g., `support@yourdomain.com`) |
| `[GITHUB_PAGES_URL]` | Final hosted URL (e.g., `https://yourname.github.io/ai-token-metrix-privacy/`) |
| `[Bundle Identifier]` | Actual bundle ID (e.g., `com.wpf.aitokenmetrix`) |
| `[App Group Identifier]` | Actual App Group ID (e.g., `group.com.wpf.aitokenmetrix`) |

Quick bulk-replace on macOS:

```bash
cd docs/PrivacyPolicy
# example — adjust values first
sed -i '' 's/\[YOUR_NAME\]/W PF/g' en.html zh-Hans.html
sed -i '' 's/\[SUPPORT_EMAIL\]/support@example.com/g' en.html zh-Hans.html
sed -i '' 's|\[GITHUB_PAGES_URL\]|https://wpf.github.io/ai-token-metrix-privacy/|g' en.html zh-Hans.html
```

## Publishing to GitHub Pages

**Option A — Dedicated repo:**
1. Create a new public repo `ai-token-metrix-privacy`
2. Copy the four files (`index.html`, `en.html`, `zh-Hans.html`, `style.css`) to the repo root
3. Settings → Pages → Source: `Deploy from a branch` → Branch `main` / folder `/ (root)`
4. Hosted URL: `https://<username>.github.io/ai-token-metrix-privacy/`

**Option B — Serve from an existing repo's `/docs` folder:**
1. Push the entire `docs/PrivacyPolicy/` folder to your public repo
2. Settings → Pages → Source: `Deploy from a branch` → Branch `main` / folder `/docs`
3. Hosted URL: `https://<username>.github.io/<repo>/PrivacyPolicy/`

## App Store Connect submission

Paste the final URL (pointing to `index.html` or `en.html`) into:
- App Store Connect → App Information → **Privacy Policy URL** (required)
- App inside the About page (Settings → About → Privacy Policy link)

## Version updates

When updating the policy:
1. Bump "Effective Date" and "Last Updated" at the top of both `en.html` and `zh-Hans.html`
2. Also update the copy embedded inside the App
3. For material changes (e.g., iCloud sync), surface an in-App notice before the change takes effect
