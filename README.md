/* ==========================================================================
   1. CORE VIEWPORT & MOBILE RESET
   ========================================================================== */
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    font-family: 'Segoe UI', -apple-system, BlinkMacSystemFont, Arial, sans-serif;
}

body {
    background-color: #f4f6f9;
    color: #333;
    -webkit-text-size-adjust: 100%; /* Prevents mobile browsers from auto-scaling text sizes */
}

/* Changed from side-by-side display:flex to a column stack for phone screens */
.container {
    display: flex;
    flex-direction: column; 
    min-height: 100vh;
    width: 100%;
}

/* ==========================================================================
   2. MOBILE NAVIGATION HEADER (Replaced rigid desktop sidebar layout)
   ========================================================================== */
.sidebar {
    width: 100%; /* Flexible full screen width */
    background-color: #343a40;
    color: #fff;
    padding: 15px 0;
}

.sidebar .logo {
    font-size: 20px;
    font-weight: bold;
    padding: 0 15px 15px 15px;
    color: #4dabf7;
    text-align: center;
}

.nav-links {
    list-style: none;
    display: flex;
    flex-wrap: wrap; /* Allows tabs to wrap cleanly onto a second line if necessary */
    justify-content: center;
    gap: 5px;
    padding: 0 10px;
}

.nav-links li {
    flex: 1;
    min-width: 80px; /* Balances touch targets nicely across mobile screen ratios */
}

.nav-links li a {
    display: block;
    padding: 10px 5px;
    color: #c2c7d0;
    text-decoration: none;
    font-size: 0.85rem;
    font-weight: 600;
    text-align: center;
    border-radius: 6px;
    transition: 0.2s;
}

.nav-links li a:hover, .nav-links li a.active {
    background-color: rgba(255, 255, 255, 0.1);
    color: #fff;
    /* Swapped desktop left-border indicator for a clean bottom underline anchor */
    border-bottom: 3px solid #4dabf7; 
}

/* ==========================================================================
   3. CONTAINER MAIN MODULES
   ========================================================================== */
.main-content {
    flex: 1;
    padding: 15px; /* Reduced excess padding layout density for phone frames */
    width: 100%;
}

.top-bar {
    display: flex;
    flex-direction: column; /* Stack search input over admin title text on mobile */
    align-items: stretch;
    gap: 12px;
    margin-bottom: 20px;
}

/* Fixed: Erased horizontal stretch breaking 400px maximum constraint setting */
.search-bar {
    width: 100%; 
    padding: 12px 15px; /* Slightly taller touch box target for mobile taps */
    border: 1px solid #ced4da;
    border-radius: 8px;
    font-size: 16px; /* 16px minimum prevents iOS zoom-on-focus scaling */
}

.admin-profile {
    font-weight: 600;
    font-size: 0.9rem;
    text-align: center;
    color: #4a5568;
}

/* ==========================================================================
   4. CARD GRID MATRICES (Liquid Multi-Column Stack)
   ========================================================================== */
.cards-container {
    display: flex;
    flex-direction: column; /* Stacks cards vertically instead of crushing them sideways */
    gap: 12px;
    margin-bottom: 25px;
}

.card {
    width: 100%;
    padding: 20px;
    border-radius: 12px;
    color: white;
    box-shadow: 0 4px 6px rgba(0,0,0,0.02);
}

.card h3 { font-size: 14px; font-weight: 500; opacity: 0.9; }
.card .stat { font-size: 26px; font-weight: bold; margin-top: 6px; }

.blue { background-color: #3b82f6; }
.green { background-color: #10b981; }
.orange { background-color: #f59e0b; }
.purple { background-color: #8b5cf6; }

/* ==========================================================================
   5. DATA TABLES (Mobile Scrollable Area Frame Fix)
   ========================================================================== */
.table-section {
    background: white;
    padding: 15px;
    border-radius: 12px;
    box-shadow: 0 2px 8px rgba(0,0,0,0.04);
}

.table-header {
    display: flex;
    justify-content: space-between;
    align-items: center;
    margin-bottom: 15px;
    gap: 10px;
}

.table-header h2 {
    font-size: 1.1rem;
}

.btn-add {
    background-color: #2563eb;
    color: white;
    border: none;
    padding: 8px 14px;
    border-radius: 6px;
    font-weight: 600;
    font-size: 0.85rem;
    cursor: pointer;
}

/* Essential: Wraps raw data tables inside a side-scrollable window block 
   so wide text data never distorts your main app layout bounds */
.table-responsive-wrapper {
    width: 100%;
    overflow-x: auto;
    -webkit-overflow-scrolling: touch; /* Smooth inertia scrolling for touch devices */
}

table {
    width: 100%;
    border-collapse: collapse;
    white-space: nowrap; /* Keeps rows neat and scrollable on thin screens */
}

th, td {
    text-align: left;
    padding: 12px 10px;
    border-bottom: 1px solid #edf2f7;
    font-size: 0.85rem;
}

th { color: #718096; font-size: 12px; text-transform: uppercase; letter-spacing: 0.5px; }

.badge {
    padding: 4px 8px;
    border-radius: 6px;
    font-size: 11px;
    font-weight: 600;
    display: inline-block;
}
.badge.available { background-color: #d1fae5; color: #065f46; }
.badge.issued { background-color: #e0f2fe; color: #0369a1; }

.btn-edit {
    background: none;
    border: 1px solid #cbd5e1;
    padding: 6px 12px;
    border-radius: 6px;
    color: #4a5568;
    font-weight: 600;
    cursor: pointer;
}
