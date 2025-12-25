# Testing Dark Mode

## Quick Testing Options

### Option 1: Interactive Demo (Recommended)
The easiest way to test the dark mode implementation:

1. Open `dark-mode-demo.html` in your browser:
   ```bash
   # In the project directory
   open dark-mode-demo.html  # macOS
   # or
   xdg-open dark-mode-demo.html  # Linux
   # or just drag the file to your browser
   ```

2. Click the buttons to toggle between:
   - ☀️ Light Mode only
   - 🌙 Dark Mode only
   - 👁️ Compare Both side-by-side

### Option 2: Test with Browser DevTools
1. Open `test-preview.html` in your browser
2. Open DevTools (F12)
3. Press `Cmd/Ctrl + Shift + P` to open Command Palette
4. Type "Rendering" and select "Show Rendering"
5. Find "Emulate CSS media feature prefers-color-scheme"
6. Toggle between `light` and `dark` to see the changes

### Option 3: Test with System Settings
1. Open `test-preview.html` in your browser
2. Change your system's appearance settings:
   - **macOS**: System Preferences → General → Appearance → Dark
   - **Windows 10/11**: Settings → Personalization → Colors → Dark
   - **Linux (GNOME)**: Settings → Appearance → Dark
3. The page should automatically switch to dark mode

### Option 4: Local Jekyll Server
If you have Jekyll installed:

```bash
# Install dependencies (first time only)
gem install jekyll bundler

# Serve the site locally
jekyll serve

# Visit http://localhost:4000
```

Then use any of the browser testing methods above.

## What to Look For

When testing dark mode, verify:

✅ **Background colors** switch from light to dark
✅ **Text colors** are readable with good contrast
✅ **Links** are clearly visible in both modes
✅ **Code blocks** have appropriate syntax highlighting
✅ **Navigation** is clearly visible
✅ **Borders and dividers** are visible but not harsh
✅ **Widget area** (sidebar) adapts correctly
✅ **Footer** text is readable

## Testing Checklist

- [ ] Homepage displays correctly in light mode
- [ ] Homepage displays correctly in dark mode
- [ ] Blog post content is readable in both modes
- [ ] Code syntax highlighting works in both modes
- [ ] Links are distinguishable and readable
- [ ] Navigation menu is functional in both modes
- [ ] Sidebar widgets adapt to dark mode
- [ ] Footer is readable in both modes
- [ ] Smooth transition between modes
- [ ] No color contrast accessibility issues

## Browser Compatibility

The dark mode should work in:
- ✅ Chrome/Edge 76+
- ✅ Firefox 67+
- ✅ Safari 12.1+
- ✅ Opera 62+

## Automated Testing (Advanced)

If you want to capture screenshots programmatically:

### Using Chrome Headless
```bash
# Light mode screenshot
google-chrome --headless --screenshot=light-mode.png --window-size=1280,1024 \
  --force-color-profile=srgb test-preview.html

# Dark mode screenshot (requires Chrome 96+)
google-chrome --headless --screenshot=dark-mode.png --window-size=1280,1024 \
  --force-color-profile=srgb --force-dark-mode test-preview.html
```

### Using Firefox Screenshot
```bash
firefox --screenshot light-mode.png test-preview.html
```

## GitHub Pages Deployment

Once merged to the main branch, test on the live site:
- Visit https://rlbisbe.net
- Use browser DevTools to toggle dark mode
- Verify all pages render correctly

## Troubleshooting

**Dark mode not activating?**
- Check that `dark-mode.css` is loaded (DevTools → Network tab)
- Verify browser supports `prefers-color-scheme` media query
- Try hard refresh (Cmd/Ctrl + Shift + R)

**Colors look wrong?**
- Check browser zoom level (should be 100%)
- Verify no browser extensions are interfering with CSS
- Clear browser cache

**Iframe not showing content?**
- If testing locally, make sure you're serving via HTTP, not file://
- Use `python3 -m http.server 8000` and visit http://localhost:8000/dark-mode-demo.html
