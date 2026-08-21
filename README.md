# Viber Template Management - Interactive Demo

A fully interactive HTML mockup/prototype of a Viber template management interface for CPaaS platforms.

## What's Included

- **Sidebar Navigation** - Full navigation menu with GMS branding
- **Template List** - Searchable, filterable table of Viber templates
- **Template Management** - Add, view, and delete templates
- **Viber ID Management** - Modal showing connected Viber business accounts
- **Advanced Filters** - Filter by Language, Status, and Category
- **Add Template Modal** - Full-screen form with live preview
- **Template Details** - View modal showing Template ID (UUID), status, and content

## Features

### Template List
- Search templates by name (real-time)
- Filter by:
  - **Language** (dynamic based on created templates)
  - **Status** (Approved, Pending, Declined)
  - **Category** (OTP, Transactional)
- Click any row to view full details
- Three-dot menu for View/Delete actions

### Create Template
- Template Name (0/64 character counter)
- Category dropdown (OTP, Transactional)
- Language dropdown (40+ options)
- Message Body (0/1000 character counter)
- Auto-detect variables with {{placeholder}} syntax
- Live preview with compliance checklist
- OTP validation (must include {{pin}})

### Viber ID Management
- View connected Viber accounts
- Shows: Business Name, Viber ID, Integration Type, Callback URLs, Status
- "Request New" button (static)

## How to Use

### Option 1: Download & Open Locally
1. Download `viber-template-management-demo.html`
2. Double-click to open in your browser
3. No internet required (uses CDN for icons)

### Option 2: View on GitHub Pages
1. Fork/Clone this repository
2. Enable GitHub Pages in repository settings
3. Set source to `main` branch
4. Access at: `https://yourusername.github.io/repository-name/viber-template-management-demo.html`

### Option 3: Share Direct Link
1. Upload the HTML file to any static hosting:
   - GitHub Pages (free)
   - Netlify (free)
   - Vercel (free)
   - AWS S3 (paid)
2. Share the link with anyone

### Option 4: Embed in Presentation/Documentation
Include the full HTML as an iframe:
```html
<iframe src="path/to/viber-template-management-demo.html" width="100%" height="800"></iframe>
```

## Sample Data

The demo comes with 12 sample templates:
- **6 Approved** templates
- **2 Pending** templates  
- **3 Declined** templates

Multiple languages: English, French, Arabic
Multiple categories: OTP, Transactional

## Viber-Specific Details

### Template ID
- Format: UUID (e.g., `2c017482-2f44-41d6-adad-2d6af725fdbr`)
- Displayed in View modal
- Required for sending messages via Viber API

### Status States
- **Approved** (green) - Ready to use
- **Pending** (amber) - Under Viber's 24-hour review
- **Declined** (red) - Rejected by Viber

### Template Categories
- **OTP** - One-Time Password messages (must include {{pin}})
- **Transactional** - Order updates, shipping, etc.

### Languages Supported
Arabic, English, French, German, Portuguese, Russian, Spanish, Turkish, and 30+ more

## Technology Stack

- **Pure HTML5** - No build tools needed
- **Vanilla JavaScript** - No frameworks
- **CSS3** - Flexbox & Grid
- **Tabler Icons** - CDN-loaded icon library

## Browser Support

- Chrome/Chromium (latest)
- Firefox (latest)
- Safari (latest)
- Edge (latest)

## Sharing with Team

### Method 1: Direct Download
```bash
curl -O https://raw.githubusercontent.com/yourusername/your-repo/main/viber-template-management-demo.html
```

### Method 2: GitHub Link
```
https://github.com/yourusername/your-repo/blob/main/viber-template-management-demo.html
```
*Click "Raw" to view and download*

### Method 3: GitHub Pages (Recommended)
```
https://yourusername.github.io/your-repo/viber-template-management-demo.html
```

### Method 4: Share Zip File
Create a release on GitHub:
1. Go to Releases
2. Create new release
3. Upload HTML file as attachment
4. Share release link

## Repository Structure

```
viber-template-management-demo/
├── viber-template-management-demo.html    # Main demo file (standalone)
├── README.md                               # This file
└── DEMO_FEATURES_SUMMARY.md               # Detailed feature list
```

## Using as Design Reference

This demo is perfect for:
- **Design Reviews** - Share with stakeholders
- **Developer Handoff** - Reference implementation
- **Team Alignment** - Visual specification
- **API Documentation** - Shows Viber API integration

## To Modify/Extend

1. Open HTML file in a text editor
2. Look for:
   - **CSS** (lines 8-132): Styling and layout
   - **HTML** (lines 135-350): Structure
   - **JavaScript** (lines 351-582): Interactivity
3. Make changes and save
4. Refresh browser to see updates

### Sample JavaScript Modifications

**Add a new template programmatically:**
```javascript
var newTemplate = {
  id: "unique-uuid-here",
  name: "template_name",
  status: "Approved",
  category: "OTP",
  language: "English",
  body: "Your code is {{pin}}"
};
templates.push(newTemplate);
renderTable(templates);
```

**Change default color scheme:**
Search and replace `#25D366` (Viber green) with your brand color

**Add new filter section:**
Duplicate a filter section in HTML and add corresponding JavaScript logic

## Limitations

- Data is stored in browser memory (resets on page refresh)
- No backend/database integration
- "+ Request New" button is static (not functional)
- Edit functionality is disabled (per Viber API restrictions)

## Future Enhancements

Potential additions:
- Backend integration with Viber API
- Database persistence
- Campaign creation flow
- Variable mapping for sending
- Webhook configuration UI
- Analytics dashboard

## License

MIT License - Free to use and modify

## Contact & Support

For questions about the demo:
- Open an Issue on GitHub
- Check the DEMO_FEATURES_SUMMARY.md for detailed feature list
- Review Viber API docs: https://www.viber.com/en/business/dev-resources/

## Related Resources

- [Viber API Documentation](https://developers.viber.com/)
- [Viber Business Solutions](https://www.viber.com/en/business/)
- [Viber Transactional Templates](https://www.viber.com/en/business/solutions/transactional-messaging/)

---

**Created:** 2026
**Last Updated:** August 2026
**Version:** 1.0
