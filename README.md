* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

body {
    font-family: "Segoe UI", Tahoma, Geneva, Verdana, sans-serif;
    background: #f4f6f9;
    color: #333;
    line-height: 1.5;
}

.container {
    display: flex;
    min-height: 100vh;
}

/* ===========================
   Sidebar
=========================== */

.sidebar {
    width: 240px;
    background: #343a40;
    color: #fff;
    padding: 20px 0;
}

.logo {
    padding: 0 20px 30px;
    font-size: 24px;
    font-weight: bold;
    color: #4dabf7;
}

.nav-links {
    list-style: none;
}

.nav-links li {
    margin-bottom: 5px;
}

.nav-links li a {
    display: block;
    padding: 12px 20px;
    text-decoration: none;
    color: #c2c7d0;
    transition: background .3s ease, color .3s ease;
}

.nav-links li a:hover,
.nav-links li a.active {
    background: rgba(255,255,255,.1);
    color: #fff;
    border-left: 4px solid #4dabf7;
}

/* ===========================
   Main Content
=========================== */

.main-content {
    flex: 1;
    padding: 30px;
}

.top-bar {
    display: flex;
    justify-content: space-between;
    align-items: center;
    margin-bottom: 30px;
    gap: 20px;
}

.search-bar {
    width: 400px;
    max-width: 100%;
    padding: 10px 15px;
    border: 1px solid #ced4da;
    border-radius: 5px;
    outline: none;
}

.search-bar:focus {
    border-color: #4dabf7;
}

.admin-profile {
    font-weight: 600;
}

/* ===========================
   Dashboard Cards
=========================== */

.cards-container {
    display: flex;
    flex-wrap: wrap;
    gap: 20px;
    margin-bottom: 40px;
}

.card {
    flex: 1 1 220px;
    padding: 20px;
    border-radius: 8px;
    color: #fff;
}

.card h3 {
    font-size: 16px;
    font-weight: 500;
}

.card .stat {
    margin-top: 10px;
    font-size: 30px;
    font-weight: bold;
}

.blue {
    background: #3b82f6;
}

.green {
    background: #10b981;
}

.orange {
    background: #f59e0b;
}

.purple {
    background: #8b5cf6;
}

/* ===========================
   Table Section
=========================== */

.table-section {
    background: #fff;
    padding: 20px;
    border-radius: 8px;
    box-shadow: 0 2px 8px rgba(0,0,0,.08);
}

.table-header {
    display: flex;
    justify-content: space-between;
    align-items: center;
    margin-bottom: 20px;
}

.btn-add {
    padding: 10px 15px;
    background: #2563eb;
    color: #fff;
    border: none;
    border-radius: 5px;
    cursor: pointer;
    transition: .3s;
}

.btn-add:hover {
    background: #1d4ed8;
}

table {
    width: 100%;
    border-collapse: collapse;
}

th,
td {
    padding: 12px 15px;
    text-align: left;
    border-bottom: 1px solid #edf2f7;
}

th {
    color: #718096;
    font-size: 13px;
    text-transform: uppercase;
}

.badge {
    display: inline-block;
    padding: 5px 10px;
    border-radius: 4px;
    font-size: 12px;
    font-weight: 600;
}

.badge.available {
    background: #d1fae5;
    color: #065f46;
}

.badge.issued {
    background: #e0f2fe;
    color: #0369a1;
}

.btn-edit {
    padding: 5px 10px;
    background: transparent;
    border: 1px solid #cbd5e1;
    border-radius: 4px;
    cursor: pointer;
    transition: .3s;
}

.btn-edit:hover {
    background: #f1f5f9;
}

/* ===========================
   Responsive
=========================== */

@media (max-width: 768px) {

    .container {
        flex-direction: column;
    }

    .sidebar {
        width: 100%;
    }

    .top-bar {
        flex-direction: column;
        align-items: stretch;
    }

    .search-bar {
        width: 100%;
    }

    .cards-container {
        flex-direction: column;
    }

    .table-section {
        overflow-x: auto;
    }
}
