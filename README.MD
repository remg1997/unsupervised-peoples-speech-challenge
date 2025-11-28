# Unsupervised Speech in the Wild Challenge

**Learning Robust Multilingual Representations from Unsupervised People's Speech**

Official website for the USW Challenge at Interspeech 2026.

## Local Development

To preview the site locally, you can use any static file server:

```bash
# Using Python
python -m http.server 8000

# Using Node.js (npx)
npx serve .

# Using PHP
php -S localhost:8000
```

Then open http://localhost:8000 in your browser.

## GitHub Pages Setup

### Enable GitHub Pages

1. Go to your repository on GitHub
2. Click **Settings** > **Pages** (in the left sidebar)
3. Under **Source**, select **Deploy from a branch**
4. Select **main** branch and **/ (root)** folder
5. Click **Save**

Your site will be available at: `https://<username>.github.io/<repo-name>/`

### Custom Domain with Namecheap

#### Step 1: Purchase Domain on Namecheap
Purchase your desired domain (e.g., `usw-challenge.org`) on Namecheap.

#### Step 2: Configure DNS on Namecheap

1. Log in to Namecheap and go to **Domain List**
2. Click **Manage** next to your domain
3. Go to **Advanced DNS** tab
4. Delete any existing A Records or CNAME records for @ or www
5. Add the following DNS records:

| Type | Host | Value | TTL |
|------|------|-------|-----|
| A Record | @ | 185.199.108.153 | Automatic |
| A Record | @ | 185.199.109.153 | Automatic |
| A Record | @ | 185.199.110.153 | Automatic |
| A Record | @ | 185.199.111.153 | Automatic |
| CNAME | www | `<username>.github.io` | Automatic |

Replace `<username>` with your GitHub username.

#### Step 3: Configure GitHub Pages

1. Create a file named `CNAME` in the root of your repository containing only your domain:
   ```
   usw-challenge.org
   ```

2. In GitHub repository **Settings** > **Pages**:
   - Enter your custom domain (e.g., `usw-challenge.org`)
   - Check **Enforce HTTPS** (after DNS propagates)

#### Step 4: Wait for DNS Propagation
DNS changes can take up to 24-48 hours to propagate. You can check status with:
```bash
dig usw-challenge.org +short
```

### HTTPS

GitHub Pages provides free HTTPS via Let's Encrypt. After DNS is configured:
1. Go to **Settings** > **Pages**
2. Check **Enforce HTTPS**

## Project Structure

```
.
├── index.html              # Main challenge webpage
├── css/
│   └── style.css          # Stylesheet
├── js/
│   └── main.js            # Interactive features
├── images/
│   └── organizers/        # Organizer photos
│       └── placeholder.svg
├── CNAME                   # Custom domain (create after purchase)
├── challenge-proposal.md   # Original proposal document
└── README.MD              # This file
```

## Adding Organizer Photos

Replace `images/organizers/placeholder.svg` with actual photos:

1. Add photos to `images/organizers/` (recommended: 200x200px, JPG/PNG)
2. Update `index.html` to reference the new images:
   ```html
   <img src="images/organizers/rafael.jpg" alt="Rafael Mosquera-Gómez">
   ```

## Timeline

- **Dec 12, 2025**: Release & Baselines
- **Feb 25, 2026**: Paper Submission Deadline
- **Mar 4, 2026**: Paper Update Deadline
- **Apr 24 – May 1, 2026**: Rebuttal Period
- **Jun 5, 2026**: Paper Acceptance Notification
- **Jun 19, 2026**: Camera-Ready Submission
- **Sep 27 – Oct 1, 2026**: Interspeech 2026

## Organizers

- Rafael Mosquera-Gómez (MLCommons / Factored AI)
- Dr. Sarah Luger (MLCommons / iMerit)
- Daniel Galvez (NVIDIA)
- Sheriff Issaka (UCLA / All Lab)
- Chiara Bonfanti (Politecnico di Torino)
- Chris Emezue (Mila / Lanfrica)
- Juan Felipe Rodríguez (Factored AI)

## License

This website content is for the USW Challenge at Interspeech 2026.
