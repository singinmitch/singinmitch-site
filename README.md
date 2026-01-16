# SinginMitch Landing Page

Your custom affiliate bridge page for TikTok and beyond.

---

## 🚀 Deployment Instructions

### Step 1: Deploy to Netlify

**Option A: Drag & Drop (Easiest)**
1. Go to [netlify.com](https://netlify.com) and sign up/log in
2. From your dashboard, click **"Add new site"** → **"Deploy manually"**
3. Drag and drop this entire folder onto the upload area
4. Your site will be live in seconds at `random-name.netlify.app`

**Option B: GitHub (Recommended for updates)**
1. Create a GitHub account if you don't have one
2. Create a new repository (e.g., `singinmitch-site`)
3. Upload all these files to the repository
4. In Netlify, click **"Add new site"** → **"Import an existing project"**
5. Connect your GitHub and select the repository
6. Click **"Deploy site"**

---

### Step 2: Connect Your Domain (SinginMitch.com)

1. In Netlify, go to **Site settings** → **Domain management**
2. Click **"Add custom domain"**
3. Enter: `singinmitch.com`
4. Click **"Verify"** → **"Yes, add domain"**
5. Click **"Options"** → **"Set up Netlify DNS"**
6. You'll see 4 nameservers like:
   ```
   dns1.p01.nsone.net
   dns2.p01.nsone.net
   dns3.p01.nsone.net
   dns4.p01.nsone.net
   ```

---

### Step 3: Update Namecheap

1. Log into [Namecheap](https://namecheap.com)
2. Go to **Domain List** → click **"Manage"** next to singinmitch.com
3. Scroll to **"Nameservers"**
4. Select **"Custom DNS"**
5. Enter the 4 Netlify nameservers (one per line)
6. Click the **green checkmark** to save

**Wait 15 minutes to 24 hours for DNS to propagate.**

---

### Step 4: SSL Certificate (Automatic!)

Once DNS propagates:
1. Go back to Netlify **Domain management**
2. Netlify will automatically provision a free SSL certificate
3. Your site will be live at `https://singinmitch.com` 🎉

---

## 📝 How to Update Your Links

Open `index.html` in any text editor and find/replace:

### Update NordVPN Link
Find this line:
```html
<a href="#" class="link-card" target="_blank" rel="noopener noreferrer" id="nordvpn-link">
```
Replace `#` with your actual NordVPN affiliate link.

### Update Amazon Links
Find and replace `YOUR_AMAZON_TAG` with your actual Amazon Associates tag.

For the Neumann TLM 103:
```html
<a href="https://www.amazon.com/dp/B00009URPJ?tag=YOUR_AMAZON_TAG"
```

For the Boss RC-505 MK2:
```html
<a href="https://www.amazon.com/dp/B09NRZS19N?tag=YOUR_AMAZON_TAG"
```

### Update Social Links
Find these lines and update the URLs:
```html
<a href="https://tiktok.com/@singinmitch"
<a href="https://youtube.com/@singinmitch"
<a href="https://instagram.com/singinmitch"
<a href="https://open.spotify.com/artist/singinmitch"
```

---

## ➕ Adding New Links

To add a new affiliate link, copy this template and paste it in the appropriate section:

```html
<a href="YOUR_LINK_HERE" class="link-card" target="_blank" rel="noopener noreferrer">
    <div class="link-icon" style="background: linear-gradient(135deg, #1a1a1a 0%, #2a2a2a 100%); color: #ffffff;">
        <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
            <!-- Add appropriate SVG icon here -->
            <circle cx="12" cy="12" r="10"/>
        </svg>
    </div>
    <div class="link-content">
        <div class="link-title">Product Name</div>
        <div class="link-description">Short description here</div>
    </div>
    <div class="link-arrow">
        <svg width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
            <path d="M5 12h14"/>
            <path d="m12 5 7 7-7 7"/>
        </svg>
    </div>
</a>
```

---

## 📁 File Structure

```
singinmitch-site/
├── index.html          # Main landing page
├── netlify.toml        # Netlify configuration
├── README.md           # This file
└── images/
    └── mitch-profile.jpg   # Your profile photo
```

---

## 🎨 Customization Tips

### Change Colors
Edit the CSS variables at the top of `index.html`:
```css
:root {
    --accent-primary: #3b82f6;    /* Main accent color */
    --accent-secondary: #60a5fa;  /* Secondary accent */
    --bg-primary: #0a0a0b;        /* Background */
    /* ... etc */
}
```

### Change Profile Photo
Replace `images/mitch-profile.jpg` with a new image (keep the same filename) or update the `src` in the HTML.

---

## 📊 Analytics (Optional)

To track clicks, add Google Analytics or use UTM parameters:
```
https://try.elevenlabs.io/f94apjzgx6na?utm_source=singinmitch&utm_medium=linkinbio
```

---

## Need Help?

- [Netlify Docs](https://docs.netlify.com)
- [Namecheap DNS Guide](https://www.namecheap.com/support/knowledgebase/article.aspx/767/10/how-to-change-dns-for-a-domain/)

Good luck! 🎤✨
