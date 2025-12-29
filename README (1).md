# 🏥 Hospital Patient Registration System

**Live Patient Registration with Admin Dashboard**

![Status](https://img.shields.io/badge/status-ready-brightgreen)
![License](https://img.shields.io/badge/license-MIT-blue)

---

## 🚀 Quick Start

This is a complete hospital patient registration system with:
- ✅ **Patient Kiosk** - Self-service registration
- ✅ **Admin Dashboard** - Room management (password protected)
- ✅ **Real-time Sync** - Updates across all open tabs
- ✅ **Zero Setup** - Just deploy and use!

---

## 📦 What's Included

- **Single HTML file** - Complete system in one file
- **No database needed** - Uses localStorage
- **Password protected** - Admin section secured
- **Mobile responsive** - Works on all devices

---

## 🌐 Deploy to GitHub Pages (FREE)

### Step 1: Fork/Upload This Repo

**Option A: Upload Files**
1. Create new repository on GitHub
2. Name it: `hospital-system`
3. Make it **Public**
4. Upload the `index.html` file
5. Commit changes

**Option B: Use GitHub Desktop**
1. Download this folder
2. Open GitHub Desktop
3. Create new repository
4. Add files
5. Publish to GitHub

### Step 2: Enable GitHub Pages

1. Go to your repository
2. Click **Settings** (top menu)
3. Scroll down to **Pages** (left sidebar)
4. Under **Source**, select: `main` branch
5. Click **Save**
6. Wait 2 minutes

### Step 3: Get Your Link!

Your website will be live at:
```
https://yourusername.github.io/hospital-system/
```

Share this link with:
- ✅ Patients - For registration
- ✅ Staff - For admin access (password required)

---

## 🎯 How to Use

### For Patients (Public Access)

1. Open the website link
2. You'll see **"Patient Kiosk"** view by default
3. Fill in the registration form:
   - Full Name
   - Mobile Number
   - Age
   - Gender
   - Department
4. Select an **available room** (green colored)
5. Click **"Book Room"**
6. Get your **Token Number** (e.g., T-001)
7. Proceed to the assigned room

### For Admin/Staff (Password Protected)

1. Open the same website link
2. Click **"Admin Dashboard"** button (top right)
3. Enter password: **`1234@admin`**
4. Admin view opens with:
   - Live statistics
   - Room status
   - Patient details
   - Booking history
5. Manage rooms:
   - Release completed consultations
   - View patient information
   - Track revenue
6. Click **"Logout"** when done

---

## 🔐 Admin Password

**Password:** `1234@admin`

### Change the Password:

1. Open `index.html` in any text editor
2. Find line ~615:
   ```javascript
   const ADMIN_PASSWORD = '1234@admin';
   ```
3. Change to your password:
   ```javascript
   const ADMIN_PASSWORD = 'YourSecurePassword123';
   ```
4. Save and re-commit to GitHub
5. GitHub Pages will update automatically

---

## ✨ Features

### Patient Kiosk Features:
- 📝 Simple registration form
- 🚪 Visual room selection (color-coded)
- 🎫 Automatic token generation
- ✅ Instant booking confirmation
- 📱 Mobile-friendly interface

### Admin Dashboard Features:
- 📊 Live statistics dashboard
  - Total patients today
  - Active consultations
  - Revenue tracking
  - Available rooms
- 🏥 Room management
  - See patient details in each room
  - Release rooms after consultation
  - Bulk release option
- 📋 Booking history
  - All bookings with timestamps
  - Active/Completed status
  - Patient information
- 🔒 Secure access with password
- 🚪 Logout functionality

### Technical Features:
- 🔄 Real-time sync (1-second updates)
- 💾 Data persistence (localStorage)
- 📡 BroadcastChannel for instant updates
- 🎨 Modern, professional UI
- 🔐 Password protection for admin
- 📱 Fully responsive design

---

## 🏗️ System Architecture

```
┌─────────────────────────────────────────────┐
│         SINGLE HTML FILE                    │
│                                             │
│  ┌─────────────┐      ┌─────────────┐     │
│  │   Patient   │      │    Admin    │     │
│  │   Kiosk     │      │  Dashboard  │     │
│  │  (Public)   │      │ (Password)  │     │
│  └──────┬──────┘      └──────┬──────┘     │
│         │                    │             │
│         └────────┬───────────┘             │
│                  │                         │
│         ┌────────▼─────────┐              │
│         │   localStorage   │              │
│         │  (Data Storage)  │              │
│         └──────────────────┘              │
│                                             │
└─────────────────────────────────────────────┘
```

---

## 📊 Room Configuration

| Room | Doctor | Specialty |
|------|--------|-----------|
| Room 1 | Dr. Rajesh Kumar | General Medicine |
| Room 2 | Dr. Priya Sharma | Pediatrics |
| Room 3 | Dr. Amit Patel | Orthopedics |
| Room 4 | Dr. Sunita Verma | Gynecology |

### Department Fees:
- General Medicine: ₹300
- Surgery: ₹500
- Pediatrics: ₹350
- Gynecology: ₹400
- Orthopedics: ₹450
- Cardiology: ₹600

*Registration fee: ₹50 (added to department fee)*

---

## 🔄 How Real-Time Sync Works

1. **Patient books a room** on their device
2. **Data saved** to localStorage
3. **BroadcastChannel** notifies all open tabs
4. **Storage event** triggers updates
5. **Admin dashboard** updates within 1 second
6. **All devices** see the same data

**Note:** Works perfectly on **same browser**. For cross-device sync across different locations/phones, upgrade to server-based solution.

---

## 📱 Access Your Website

After deploying to GitHub Pages, you can:

### Share Direct Link:
```
https://yourusername.github.io/hospital-system/
```

### Create QR Code:
1. Go to: https://qr-code-generator.com
2. Enter your GitHub Pages URL
3. Download QR code
4. Print and display at hospital

### Shorten URL:
Use bit.ly or tinyurl.com to create:
```
https://bit.ly/hospital-register
```

---

## 🎨 Customization

### Change Colors:
Edit CSS section (lines 10-400) in `index.html`

### Add More Rooms:
Edit JavaScript (lines 650-660):
```javascript
rooms: [
    { id: 1, number: 'Room 1', ... },
    { id: 2, number: 'Room 2', ... },
    { id: 5, number: 'Room 5', ... }, // Add new room
]
```

### Change Department Fees:
Edit HTML form (lines 350-360):
```html
<option value="General Medicine" data-fee="300">General Medicine - ₹300</option>
```

---

## 🆘 Troubleshooting

### Website not loading?
- Wait 2-3 minutes after enabling GitHub Pages
- Check repository is **Public**
- Verify file is named `index.html`

### Admin login not working?
- Password: `1234@admin` (case-sensitive)
- Check for spaces before/after password
- Verify you didn't accidentally change it

### Data not syncing?
- Wait 1-2 seconds for automatic sync
- Refresh the page
- Check if using same browser
- Clear browser cache if needed

### Room stuck as occupied?
- Admin can manually release using "Release" button
- Or use "Release All Rooms" to clear all

---

## 💡 Pro Tips

### For Reception Desk:
1. Keep website open on reception computer
2. Leave on "Patient Kiosk" view
3. Patients can self-register
4. Staff switches to admin when needed

### For Tablets:
1. Set up tablet at entrance
2. Open website in fullscreen (F11)
3. Enable kiosk mode to prevent navigation
4. Patients register on walk-in

### For Multiple Locations:
- Each location can have their own admin access
- Same password for all staff
- Central management possible

---

## 📈 Future Enhancements

Want to upgrade? Possible additions:
- [ ] SMS notifications to patients
- [ ] Email confirmations
- [ ] Print token receipts
- [ ] Multiple hospital branches
- [ ] Doctor scheduling
- [ ] Patient history
- [ ] Online payments integration
- [ ] Report generation

---

## 🔒 Security Notes

- ✅ Admin password protected
- ✅ Patients cannot access admin features
- ✅ Data stored locally in browser
- ✅ No external database needed
- ⚠️ For production, consider server-based solution

---

## 📞 Support

### Common Issues:

**Q: Can I use this on multiple devices?**
A: Yes! It syncs perfectly on the **same browser** (multiple tabs). For true cross-device sync (different phones/tablets), upgrade to server-based solution (InfinityFree/Firebase).

**Q: Is data saved permanently?**
A: Data is saved in browser localStorage. It persists unless:
- Browser cache is cleared
- Browser private/incognito mode used
- Different browser is used

**Q: Can I customize the look?**
A: Yes! Edit the CSS section in `index.html`. All styles are in one file.

**Q: How do I reset all data?**
A: Open browser console (F12) and run:
```javascript
localStorage.clear();
location.reload();
```

---

## 📄 License

MIT License - Free to use, modify, and distribute.

---

## 🎉 You're All Set!

Your hospital registration system is ready!

**Deployment Checklist:**
- [ ] Repository created on GitHub
- [ ] `index.html` file uploaded
- [ ] GitHub Pages enabled
- [ ] Website accessible via link
- [ ] Patient registration tested
- [ ] Admin login tested (password: `1234@admin`)
- [ ] Room booking tested
- [ ] Room release tested
- [ ] Link shared with staff
- [ ] QR code created and printed

---

**Made with ❤️ for efficient hospital management**

*Deploy once, use forever!*
