<template>
  <div id="app">
    <div class="layout">
      <!-- Sidebar -->
      <aside class="sidebar">
        <div class="sidebar-header">
          <h2>App Menu</h2>
        </div>
        <nav class="sidebar-nav">
          <a href="#" class="nav-item active">
            <span class="icon">📊</span>
            <span>Dashboard</span>
          </a>

          <a href="#" class="nav-item">
            <span class="icon">🏷️</span>
            <span>Offers</span>
          </a>

          <a href="#" class="nav-item">
            <span class="icon">⚙️</span>
            <span>Settings</span>
          </a>
        </nav>
      </aside>

      <!-- Main content -->
      <main class="main-content">
        <div class="content-wrapper">
          <h1>Dashboard</h1>

          <section class="content-section">
            <h2>Overview</h2>
            <div class="cards-grid">
              <div class="card">
                <div class="card-label">Total Items</div>
                <div class="card-value">24</div>
              </div>
              <div class="card">
                <div class="card-label">Active</div>
                <div class="card-value">18</div>
              </div>
              <div class="card">
                <div class="card-label">Pending</div>
                <div class="card-value">6</div>
              </div>
            </div>
          </section>
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
  height: 100vh;
}

.layout {
  display: flex;
  height: 100%;
}

/* Sidebar */
.sidebar {
  width: 240px;
  background: #2d2d2d;
  color: white;
}

.sidebar-header {
  padding: 24px;
  background: #1a1a1a;
  border-bottom: 1px solid #444;
}

.sidebar-header h2 {
  font-size: 16px;
  font-weight: 600;
  color: #fff;
}

.sidebar-nav {
  padding: 16px 0;
}

.nav-item {
  display: flex;
  align-items: center;
  gap: 12px;
  padding: 12px 24px;
  color: #ccc;
  text-decoration: none;
  cursor: pointer;
  font-size: 14px;
  transition: all 0.2s;
}

.nav-item:hover {
  background: #3a3a3a;
  color: white;
}

.nav-item.active {
  background: #3a3a3a;
  color: white;
  border-left: 3px solid #4285f4;
}

.nav-item .icon {
  font-size: 18px;
}

/* Main content */
.main-content {
  flex: 1;
  background: #f5f5f5;
  overflow-y: auto;
}

.content-wrapper {
  padding: 32px;
  max-width: 1200px;
}

.content-wrapper h1 {
  font-size: 32px;
  font-weight: 600;
  color: #2c3e50;
  margin-bottom: 32px;
}

.content-section {
  margin-bottom: 32px;
}

.content-section h2 {
  font-size: 18px;
  font-weight: 600;
  color: #2c3e50;
  margin-bottom: 16px;
}

.cards-grid {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 20px;
}

.card {
  background: white;
  border: 1px solid #e0e0e0;
  border-radius: 8px;
  padding: 24px;
}

.card-label {
  color: #666;
  font-size: 14px;
  margin-bottom: 8px;
}

.card-value {
  font-size: 36px;
  font-weight: 600;
  color: #2c3e50;
}
</style>
