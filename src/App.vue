<template>
  <div id="app">
    <div class="layout">
      <!-- Sidebar -->
      <aside class="sidebar">
        <div class="sidebar-header">
          <h2>Portal Suite</h2>
        </div>
        <nav class="sidebar-nav">
          <a href="#" class="nav-item active">
            <span>📊</span> Dashboard
          </a>
          <a href="#" class="nav-item">
            <span>📅</span> Appointments
            <span class="badge">14</span>
          </a>
          <a href="#" class="nav-item">
            <span>👥</span> Clients
          </a>
          <a href="#" class="nav-item">
            <span>⚙️</span> System Settings
          </a>
        </nav>
      </aside>

      <!-- Main content -->
      <main class="main-content">
        <div class="content-header">
          <h1>Dashboard</h1>
          <button class="btn-primary">+ Create New</button>
        </div>

        <!-- Stats cards -->
        <div class="stats-grid">
          <div class="stat-card">
            <div class="stat-label">Total Appointments</div>
            <div class="stat-value">142</div>
          </div>
          <div class="stat-card">
            <div class="stat-label">Active Clients</div>
            <div class="stat-value">89</div>
          </div>
          <div class="stat-card">
            <div class="stat-label">Pending</div>
            <div class="stat-value">14</div>
          </div>
          <div class="stat-card">
            <div class="stat-label">Completed</div>
            <div class="stat-value">128</div>
          </div>
        </div>

        <!-- Table -->
        <div class="table-container">
          <h2>Recent Appointments</h2>
          <table class="data-table">
            <thead>
              <tr>
                <th>ID</th>
                <th>Client</th>
                <th>Date</th>
                <th>Status</th>
                <th>Actions</th>
              </tr>
            </thead>
            <tbody>
              <tr>
                <td>#001</td>
                <td>John Doe</td>
                <td>2026-01-18</td>
                <td><span class="status pending">Pending</span></td>
                <td><button class="btn-small">View</button></td>
              </tr>
              <tr>
                <td>#002</td>
                <td>Jane Smith</td>
                <td>2026-01-19</td>
                <td><span class="status confirmed">Confirmed</span></td>
                <td><button class="btn-small">View</button></td>
              </tr>
              <tr>
                <td>#003</td>
                <td>Bob Johnson</td>
                <td>2026-01-20</td>
                <td><span class="status completed">Completed</span></td>
                <td><button class="btn-small">View</button></td>
              </tr>
            </tbody>
          </table>
        </div>
      </main>
    </div>
  </div>
</template>

<script>
export default {
  name: 'App'
}
</script>

<style>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

#app {
  font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Arial, sans-serif;
  color: #2c3e50;
  height: 100vh;
}

.layout {
  display: flex;
  height: 100%;
}

/* Sidebar */
.sidebar {
  width: 240px;
  background: #1a1a1a;
  color: white;
  padding: 20px 0;
}

.sidebar-header {
  padding: 0 20px 30px;
  border-bottom: 1px solid #333;
}

.sidebar-header h2 {
  font-size: 18px;
  font-weight: 600;
}

.sidebar-nav {
  padding-top: 20px;
}

.nav-item {
  display: flex;
  align-items: center;
  gap: 12px;
  padding: 12px 20px;
  color: #aaa;
  text-decoration: none;
  transition: all 0.2s;
}

.nav-item:hover {
  background: #252525;
  color: white;
}

.nav-item.active {
  background: #333;
  color: white;
  border-left: 3px solid #4CAF50;
}

.nav-item span:first-child {
  font-size: 18px;
}

.badge {
  margin-left: auto;
  background: #f44336;
  color: white;
  padding: 2px 8px;
  border-radius: 10px;
  font-size: 11px;
  font-weight: 600;
}

/* Main content */
.main-content {
  flex: 1;
  background: #f5f5f5;
  overflow-y: auto;
  padding: 30px;
}

.content-header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin-bottom: 30px;
}

.content-header h1 {
  font-size: 28px;
  font-weight: 600;
}

.btn-primary {
  background: #4CAF50;
  color: white;
  border: none;
  padding: 10px 20px;
  border-radius: 6px;
  cursor: pointer;
  font-size: 14px;
  font-weight: 500;
}

.btn-primary:hover {
  background: #45a049;
}

/* Stats grid */
.stats-grid {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  gap: 20px;
  margin-bottom: 30px;
}

.stat-card {
  background: white;
  padding: 20px;
  border-radius: 8px;
  border: 1px solid #e0e0e0;
}

.stat-label {
  color: #666;
  font-size: 13px;
  margin-bottom: 8px;
}

.stat-value {
  font-size: 32px;
  font-weight: 600;
  color: #2c3e50;
}

/* Table */
.table-container {
  background: white;
  padding: 24px;
  border-radius: 8px;
  border: 1px solid #e0e0e0;
}

.table-container h2 {
  font-size: 18px;
  margin-bottom: 20px;
  font-weight: 600;
}

.data-table {
  width: 100%;
  border-collapse: collapse;
}

.data-table th {
  text-align: left;
  padding: 12px;
  border-bottom: 2px solid #e0e0e0;
  font-size: 13px;
  font-weight: 600;
  color: #666;
  text-transform: uppercase;
}

.data-table td {
  padding: 16px 12px;
  border-bottom: 1px solid #f0f0f0;
}

.status {
  padding: 4px 12px;
  border-radius: 12px;
  font-size: 12px;
  font-weight: 500;
}

.status.pending {
  background: #fff3cd;
  color: #856404;
}

.status.confirmed {
  background: #d1ecf1;
  color: #0c5460;
}

.status.completed {
  background: #d4edda;
  color: #155724;
}

.btn-small {
  background: #f5f5f5;
  border: 1px solid #ddd;
  padding: 6px 16px;
  border-radius: 4px;
  cursor: pointer;
  font-size: 13px;
}

.btn-small:hover {
  background: #e0e0e0;
}
</style>
