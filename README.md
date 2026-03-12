# DiverSync - Supplier Sustainability & Diversity Risk Scorer
## Login Page & Dashboard System

### Overview
This is a web-based login and dashboard system for the **DiverSync** application - an AI-powered Supplier Sustainability and Diversity Risk Scoring platform.

### Features
- **Professional Login Page** with validation and demo credentials
- **Interactive Dashboard** with KPI cards and supplier assessment table
- **Responsive Design** that works on desktop and mobile devices
- **User Authentication** with remember me functionality
- **ESG Scoring Display** showing Environment, Social, Governance, and Diversity metrics

---

## Files Included

### 1. **login.html** - User Authentication Page
The login interface for accessing the DiverSync system.

**Features:**
- Modern, professional UI design
- Username and password input fields
- "Remember Me" functionality
- Forgot Password link
- Demo credentials auto-fill button
- Form validation with error messages
- Loading state during authentication
- Dashboard redirect after successful login

### 2. **dashboard.html** - Main Application Dashboard
The main dashboard accessible after login.

**Features:**
- Navigation bar with user info and logout button
- Key Performance Indicators (KPI) cards
- Recent supplier assessments table
- ESG and Diversity scoring categories explanation
- Action buttons for document upload, analysis, reporting, and settings
- Responsive grid layout
- Sample supplier data with color-coded risk levels

---

## Dummy User Credentials

You can login with any of the following test accounts:

| Username | Password | Role |
|----------|----------|------|
| `procurement_admin` | `SustainScore2026` | Procurement Admin |
| `supplier_auditor` | `AuditESG2026` | Supplier Auditor |
| `compliance_officer` | `Governance2026` | Compliance Officer |
| `sustainability_lead` | `SustainLeader2026` | Sustainability Lead |

### Quick Test
1. Open `login.html` in a browser
2. Click "Use Demo Credentials" button OR
3. Manually enter: Username: `procurement_admin` | Password: `SustainScore2026`
4. Click "Sign In" to access the dashboard

---

## Setup Instructions

### Option 1: Direct Browser Access
1. Navigate to the folder containing `login.html`
2. Double-click `login.html` to open in your default browser
3. Or right-click → Open with → Choose your preferred browser

### Option 2: Local Server (Recommended)
For production use, run a local server:

**Using Python 3:**
```bash
cd c:\Users\GENAIMXCDMXUSR37\Desktop\DiverSync
python -m http.server 8000
```

Then open: `http://localhost:8000/login.html`

**Using Python 2:**
```bash
python -m SimpleHTTPServer 8000
```

**Using Node.js (http-server):**
```bash
npm install -g http-server
http-server
```

**Using PHP:**
```bash
php -S localhost:8000
```

---

## Page Features & Components

### Login Page Components
- **Logo Section**: Application branding and title
- **Demo Credentials Box**: Displays test credentials
- **Username/Password Fields**: User input with focus states
- **Remember Me Checkbox**: Saves username in browser storage
- **Forgot Password Link**: Password recovery flow
- **Sign In Button**: Primary action button
- **Demo Credentials Button**: Auto-fills test credentials
- **Request Access Link**: New account registration

### Dashboard Components
- **Navigation Bar**: User profile, role, and logout button
- **Header**: Welcome message and page title
- **Action Buttons**: Quick access to key features
  - Upload Supplier Documents
  - Run ESG Scoring Analysis
  - View Reports
  - Configure Scoring Criteria

- **KPI Cards** (6 cards showing):
  - Total Suppliers (248 active, 89 scored)
  - Average ESG Score (72.5/100)
  - Risk Alerts (12 high risk, 24 medium)
  - Environmental Compliance (68%)
  - Diversity Score (64.2/100)
  - Governance Status (78/100)

- **Supplier Assessment Table**: Shows sample data with:
  - Supplier names
  - ESG scores (Environment, Social, Governance, Diversity)
  - Overall composite score
  - Risk level badges (High/Medium/Low)
  - View action button

- **Scoring Categories Table**: Explains:
  - Environment (30% weight)
  - Social (25% weight)
  - Governance (25% weight)
  - Diversity (20% weight)

---

## Functionality Details

### Login Page JavaScript
- **Form Validation**: Checks for empty fields
- **Credential Verification**: Validates against dummy user database
- **"Remember Me"**: Saves username to localStorage
- **Loading State**: Shows spinner during authentication
- **Error Messages**: Displays validation and authentication errors
- **Auto-focus**: Moves focus to password field on error
- **Enter Key Support**: Allows form submission via Enter key
- **Redirect**: Routes to dashboard.html on successful login
- **Forgot Password**: Shows email notification (simulation)

### Dashboard JavaScript
- **User Info Loading**: Retrieves current logged-in user
- **Action Handlers**: Alert messages for button clicks
- **Logout Confirmation**: Confirms before clearing session
- **Dynamic User Display**: Shows username in navbar

---

## Scoring System Explanation

### ESG Framework
1. **Environment (30% weight)**
   - Carbon emission reduction targets
   - Water management practices
   - Waste reduction programs
   - Renewable energy adoption

2. **Social (25% weight)**
   - Fair labor practices
   - Worker health & safety standards
   - Community impact programs
   - Human rights compliance

3. **Governance (25% weight)**
   - Board diversity metrics
   - Ethical compliance programs
   - Audit trail management
   - Policy documentation

4. **Diversity (20% weight)**
   - Minority-owned business status
   - Women-led business initiatives
   - Inclusive hiring practices
   - Diversity supplier programs

### Risk Levels
- **High Risk (Red)**: Score < 60 - Requires immediate corrective action
- **Medium Risk (Orange)**: Score 60-75 - Improvements needed
- **Low Risk (Green)**: Score > 75 - Meeting standards

---

## Sample Supplier Data

### GreenTech Industries (Score: 78.3 - Low Risk)
- Environment: 82 | Social: 75 | Governance: 88 | Diversity: 68

### EcoSupply Corp (Score: 66.0 - Medium Risk)
- Environment: 65 | Social: 52 | Governance: 71 | Diversity: 76

### SustainTrade Global (Score: 82.3 - Low Risk)
- Environment: 84 | Social: 79 | Governance: 85 | Diversity: 81

### MfgPartners Ltd (Score: 48.3 - High Risk)
- Environment: 48 | Social: 45 | Governance: 62 | Diversity: 38

### DiverseSource Inc (Score: 78.5 - Low Risk)
- Environment: 70 | Social: 82 | Governance: 74 | Diversity: 88

---

## Browser Compatibility
- ✅ Chrome 60+
- ✅ Firefox 55+
- ✅ Safari 12+
- ✅ Edge 79+
- ✅ Mobile browsers (iOS Safari, Chrome Mobile)

---

## Customization Guide

### Change Logo/Colors
Edit the CSS variables in the `<style>` section:
```css
/* Primary color gradient */
background: linear-gradient(135deg, #1e3c72 0%, #2a5298 100%);

/* Update logo emoji */
<div class="logo-icon">🌍</div>
```

### Add More Test Users
In `login.html`, update the `validUsers` object:
```javascript
const validUsers = {
    'username': 'password',
    'new_user': 'new_password'
};
```

### Modify Dashboard Data
Update the sample data in the HTML tables:
```html
<tr>
    <td><strong>Supplier Name</strong></td>
    <td><div class="score score-high">XX</div></td>
    <!-- Update scores and data -->
</tr>
```

### Connect to Backend API
Replace the simulated authentication with real API calls:
```javascript
// In login.html validateLogin() function
const response = await fetch('/api/login', {
    method: 'POST',
    headers: {'Content-Type': 'application/json'},
    body: JSON.stringify({username, password})
});
```

---

## File Structure
```
DiverSync/
├── login.html          (Authentication page)
├── dashboard.html      (Main application dashboard)
└── README.md          (This file)
```

---

## Next Steps - Backend Integration

To make this production-ready:

1. **Backend Authentication**
   - Create API endpoints for user login/logout
   - Implement JWT or session-based authentication
   - Secure password hashing (bcrypt, Argon2)

2. **Database**
   - Store user accounts and permissions
   - Persist supplier data and scores
   - Track score history and changes

3. **API Endpoints Needed**
   ```
   POST   /api/login              - User authentication
   POST   /api/logout             - Session termination
   GET    /api/suppliers          - Get supplier list
   POST   /api/suppliers/score    - Upload documents for scoring
   GET    /api/suppliers/{id}     - Get detailed supplier report
   POST   /api/documents/upload   - Upload ESG documents
   GET    /api/dashboard/stats    - Get KPI data
   ```

4. **AI/ML Integration**
   - Extract ESG signals from documents
   - Generate risk explanations
   - Recommend corrective actions
   - Track improvement over time

5. **Document Processing**
   - PDF text extraction
   - Natural language processing
   - Content classification
   - Evidence highlighting

---

## Support & Documentation

For more information on implementing the full ESG scoring system, refer to the problem statement and expected outputs in the specification document.

**Key deliverables to implement:**
- Supplier score per category (E/S/G/D)
- Automated evidence pack with citations
- Risk flags with corrective recommendations
- Procurement-ready summary reports

---

## License & Usage
Internal use for DiverSync application development.
Last updated: March 2026
