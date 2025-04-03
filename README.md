:root {
  --primary: #0056b3;
  --primary-hover: #004494;
  --primary-light: #e8f0fe;
  --secondary: #e63946;
  --secondary-hover: #c5303c;
  --light: #f8f9fa;
  --dark: #343a40;
  --success: #28a745;
  --warning: #ffc107;
  --danger: #dc3545;
  --gray: #6c757d;
  --gray-light: #f4f4f4;
  --border: #eee;
  --shadow: 0 2px 5px rgba(0,0,0,0.1);
  --shadow-lg: 0 5px 15px rgba(0,0,0,0.1);
  --border-radius: 8px;
  --transition: all 0.3s ease;
}

* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
}

body {
  background-color: var(--gray-light);
  color: var(--dark);
  line-height: 1.6;
}

.container {
  width: 100%;
  max-width: 1200px;
  margin: 0 auto;
  padding: 0 15px;
}

/* Header Styles */
header {
  background-color: white;
  box-shadow: var(--shadow);
  position: sticky;
  top: 0;
  z-index: 100;
}

nav {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 20px 0;
}

.logo {
  display: flex;
  align-items: center;
  font-size: 1.8rem;
  font-weight: bold;
  color: var(--primary);
}

.logo span {
  color: var(--secondary);
}

.logo i {
  margin-right: 8px;
  color: var(--secondary);
}

.nav-links {
  display: flex;
  list-style: none;
}

.nav-links li {
  margin-left: 30px;
  position: relative;
}

.nav-links a {
  text-decoration: none;
  color: var(--dark);
  font-weight: 500;
  transition: var(--transition);
  display: flex;
  align-items: center;
}

.nav-links a i {
  margin-right: 8px;
}

.nav-links a:hover {
  color: var(--primary);
}

.nav-links a::after {
  content: '';
  width: 0;
  height: 3px;
  background-color: var(--primary);
  position: absolute;
  bottom: -5px;
  left: 0;
  transition: var(--transition);
}

.nav-links a:hover::after {
  width: 100%;
}

.btn {
  padding: 10px 20px;
  border: none;
  border-radius: 5px;
  cursor: pointer;
  font-weight: 500;
  transition: var(--transition);
}

.btn-primary {
  background-color: var(--primary);
  color: white;
}

.btn-primary:hover {
  background-color: var(--primary-hover);
  transform: translateY(-2px);
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
}

.btn-secondary {
  background-color: var(--secondary);
  color: white;
}

.btn-secondary:hover {
  background-color: var(--secondary-hover);
  transform: translateY(-2px);
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
}

.btn-success {
  background-color: var(--success);
  color: white;
}

.btn-success:hover {
  background-color: #218838;
  transform: translateY(-2px);
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
}

.btn-outline-primary {
  background-color: transparent;
  color: var(--primary);
  border: 1px solid var(--primary);
}

.btn-outline-primary:hover {
  background-color: var(--primary);
  color: white;
}

/* Dashboard Styles */
.dashboard {
  padding: 40px 0;
}

.dashboard-header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin-bottom: 30px;
}

.page-title {
  font-size: 1.8rem;
  color: var(--dark);
  margin-bottom: 10px;
}

.page-subtitle {
  color: var(--gray);
  font-size: 1rem;
  font-weight: normal;
}

.panel {
  background-color: white;
  border-radius: var(--border-radius);
  box-shadow: var(--shadow);
  padding: 25px;
  margin-bottom: 25px;
  transition: var(--transition);
}

.panel:hover {
  box-shadow: var(--shadow-lg);
  transform: translateY(-5px);
}

.panel-title {
  color: var(--dark);
  margin-bottom: 15px;
  padding-bottom: 15px;
  border-bottom: 1px solid var(--border);
  display: flex;
  align-items: center;
}

.panel-title i {
  margin-right: 10px;
  color: var(--primary);
}

/* Status Tracking */
.status-card {
  position: relative;
  padding: 25px;
  border-radius: var(--border-radius);
  border-left: 5px solid var(--primary);
  background-color: white;
  box-shadow: var(--shadow);
  margin-bottom: 25px;
  transition: var(--transition);
}

.status-card:hover {
  box-shadow: var(--shadow-lg);
}

.status-title {
  font-weight: 500;
  color: var(--dark);
  display: flex;
  align-items: center;
  margin-bottom: 15px;
}

.status-title i {
  margin-right: 10px;
  color: var(--primary);
}

.status-details {
  margin-top: 15px;
  color: var(--gray);
}

.status-details p {
  margin-bottom: 10px;
}

.status-progress {
  margin: 30px 0;
}

.progress-track {
  display: flex;
  justify-content: space-between;
  position: relative;
  margin-bottom: 30px;
}

.progress-track::before {
  content: '';
  position: absolute;
  top: 15px;
  left: 14px;
  right: 14px;
  height: 4px;
  background-color: #eee;
  z-index: 1;
}

.progress-step {
  position: relative;
  z-index: 2;
  text-align: center;
}

.step-icon {
  width: 35px;
  height: 35px;
  border-radius: 50%;
  background-color: #f1f1f1;
  display: flex;
  align-items: center;
  justify-content: center;
  margin: 0 auto 8px;
  transition: var(--transition);
  border: 2px solid transparent;
  font-size: 0.9rem;
}

.step-active .step-icon {
  background-color: var(--primary);
  color: white;
  box-shadow: 0 0 0 5px rgba(0, 86, 179, 0.2);
}

.step-completed .step-icon {
  background-color: var(--success);
  color: white;
}

.step-name {
  font-size: 0.8rem;
  color: var(--gray);
  transition: var(--transition);
}

.step-active .step-name,
.step-completed .step-name {
  color: var(--dark);
  font-weight: 500;
}

/* Tabs Navigation */
.tabs {
  display: flex;
  margin-bottom: 25px;
  border-bottom: 1px solid var(--border);
  overflow-x: auto;
  scrollbar-width: thin;
}

.tabs::-webkit-scrollbar {
  height: 4px;
}

.tabs::-webkit-scrollbar-thumb {
  background-color: var(--gray);
  border-radius: 10px;
}

.tab {
  padding: 15px 25px;
  cursor: pointer;
  border-bottom: 3px solid transparent;
  margin-right: 20px;
  font-weight: 500;
  white-space: nowrap;
  transition: var(--transition);
  display: flex;
  align-items: center;
}

.tab i {
  margin-right: 8px;
}

.tab:hover {
  color: var(--primary);
}

.tab.active {
  color: var(--primary);
  border-bottom-color: var(--primary);
}

.tab-content {
  display: none;
  animation: fadeIn 0.5s;
}

@keyframes fadeIn {
  from { opacity: 0; transform: translateY(20px); }
  to { opacity: 1; transform: translateY(0); }
}

.tab-content.active {
  display: block;
}

/* Help Request Form */
.help-request-form {
  background-color: white;
  border-radius: var(--border-radius);
  box-shadow: var(--shadow);
  padding: 30px;
  margin-bottom: 30px;
}

.form-group {
  margin-bottom: 25px;
}

.form-group label {
  display: block;
  margin-bottom: 8px;
  color: var(--dark);
  font-weight: 500;
}

.form-group input,
.form-group textarea,
.form-group select {
  width: 100%;
  padding: 12px 15px;
  border: 1px solid #ddd;
  border-radius: 5px;
  font-size: 1rem;
  transition: var(--transition);
}

.form-group input:focus,
.form-group textarea:focus,
.form-group select:focus {
  outline: none;
  border-color: var(--primary);
  box-shadow: 0 0 0 3px rgba(0, 86, 179, 0.2);
}

.form-row {
  display: flex;
  margin: 0 -10px;
}

.form-col {
  flex: 1;
  padding: 0 10px;
}

/* Chat Interface */
.chat-container {
  display: flex;
  height: 70vh;
  background-color: white;
  border-radius: var(--border-radius);
  box-shadow: var(--shadow);
  overflow: hidden;
}

.chat-sidebar {
  width: 30%;
  background-color: var(--light);
  padding: 20px;
  border-right: 1px solid var(--border);
  overflow-y: auto;
}

.chat-main {
  width: 70%;
  display: flex;
  flex-direction: column;
}

.chat-header {
  padding: 15px 20px;
  border-bottom: 1px solid var(--border);
  display: flex;
  align-items: center;
}

.chat-messages {
  flex: 1;
  padding: 20px;
  overflow-y: auto;
  background-color: #f9f9f9;
}

.message {
  margin-bottom: 20px;
  display: flex;
}

.message.received {
  justify-content: flex-start;
}

.message.sent {
  justify-content: flex-end;
}

.message-content {
  max-width: 70%;
  padding: 12px 18px;
  border-radius: 18px;
  position: relative;
  box-shadow: 0 1px 3px rgba(0,0,0,0.1);
}

.received .message-content {
  background-color: white;
  color: var(--dark);
  border-bottom-left-radius: 5px;
}

.sent .message-content {
  background-color: var(--primary);
  color: white;
  border-bottom-right-radius: 5px;
}

.message-info {
  font-size: 0.8rem;
  margin-top: 5px;
}

.received .message-info {
  color: var(--gray);
}

.sent .message-info {
  color: rgba(255, 255, 255, 0.8);
  text-align: right;
}

.chat-input {
  padding: 15px;
  border-top: 1px solid var(--border);
  display: flex;
  align-items: center;
  background-color: white;
}

.chat-input input {
  flex: 1;
  padding: 12px 15px;
  border: 1px solid #ddd;
  border-radius: 30px;
  margin-right: 10px;
  font-size: 1rem;
  transition: var(--transition);
}

.chat-input input:focus {
  outline: none;
  border-color: var(--primary);
  box-shadow: 0 0 0 3px rgba(0, 86, 179, 0.2);
}

.chat-actions {
  display: flex;
  align-items: center;
  margin-right: 10px;
}

.chat-action-btn {
  background: none;
  border: none;
  color: var(--gray);
  font-size: 1.2rem;
  cursor: pointer;
  margin-right: 10px;
  transition: var(--transition);
}

.chat-action-btn:hover {
  color: var(--primary);
}

.agent-item {
  display: flex;
  align-items: center;
  padding: 15px;
  border-radius: 8px;
  cursor: pointer;
  transition: var(--transition);
  margin-bottom: 10px;
}

.agent-item:hover {
  background-color: #ebebeb;
}

.agent-item.active {
  background-color: var(--primary-light);
}

.agent-avatar {
  width: 45px;
  height: 45px;
  border-radius: 50%;
  background-color: var(--primary);
  margin-right: 15px;
  display: flex;
  align-items: center;
  justify-content: center;
  font-weight: bold;
  color: white;
}

.agent-info {
  flex: 1;
}

.agent-name {
  font-weight: 500;
  color: var(--dark);
}

.agent-status {
  font-size: 0.85rem;
  color: var(--gray);
  display: flex;
  align-items: center;
  margin-top: 3px;
}

.status-indicator {
  width: 8px;
  height: 8px;
  border-radius: 50%;
  margin-right: 5px;
  background-color: var(--gray);
}

.status-online .status-indicator {
  background-color: var(--success);
}

/* User Profile */
.user-profile {
  display: flex;
  align-items: center;
}

.profile-avatar {
  width: 40px;
  height: 40px;
  border-radius: 50%;
  background-color: var(--primary);
  color: white;
  display: flex;
  align-items: center;
  justify-content: center;
  font-weight: bold;
  margin-right: 10px;
}

.notifications-badge {
  position: relative;
  margin-left: 15px;
  cursor: pointer;
}

.badge {
  position: absolute;
  top: -5px;
  right: -5px;
  width: 18px;
  height: 18px;
  background-color: var(--secondary);
  color: white;
  border-radius: 50%;
  font-size: 0.7rem;
  display: flex;
  align-items: center;
  justify-content: center;
}

/* Vehicle Card */
.vehicle-card {
  display: flex;
  align-items: center;
  border-bottom: 1px solid var(--border);
  padding-bottom: 15px;
  margin-bottom: 15px;
}

.vehicle-icon {
  font-size: 1.8rem;
  color: var(--primary);
  margin-right: 15px;
}

.vehicle-info {
  flex: 1;
}

.vehicle-name {
  font-weight: 500;
  color: var(--dark);
}

.vehicle-details {
  font-size: 0.9rem;
  color: var(--gray);
}

/* History Cards */
.history-card {
  background-color: white;
  border-radius: var(--border-radius);
  box-shadow: var(--shadow);
  margin-bottom: 20px;
  overflow: hidden;
  transition: var(--transition);
}

.history-card:hover {
  box-shadow: var(--shadow-lg);
  transform: translateY(-5px);
}

.history-card-header {
  background-color: var(--light);
  padding: 15px 20px;
  border-bottom: 1px solid var(--border);
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.history-date {
  font-size: 0.9rem;
  color: var(--gray);
}

.history-status {
  padding: 5px 10px;
  border-radius: 20px;
  font-size: 0.8rem;
  font-weight: 500;
}

.status-completed {
  background-color: rgba(40, 167, 69, 0.1);
  color: var(--success);
}

.history-card-body {
  padding: 20px;
}

.history-card-footer {
  padding: 15px 20px;
  border-top: 1px solid var(--border);
  display: flex;
  justify-content: space-between;
  align-items: center;
}

/* Mobile Styles */
.mobile-menu-button {
  display: none;
  background: none;
  border: none;
  font-size: 1.5rem;
  color: var(--dark);
  cursor: pointer;
}

@media (max-width: 768px) {
  .mobile-menu-button {
      display: block;
  }
  
  .nav-links {
      display: none;
      position: absolute;
      top: 80px;
      left: 0;
      right: 0;
      background-color: white;
      flex-direction: column;
      padding: 20px;
      box-shadow: var(--shadow);
  }
  
  .nav-links.active {
      display: flex;
  }
  
  .nav-links li {
      margin: 10px 0;
  }
  
  .chat-container {
      flex-direction: column;
      height: auto;
  }
  
  .chat-sidebar, .chat-main {
      width: 100%;
  }
  
  .chat-sidebar {
      height: 200px;
      border-right: none;
      border-bottom: 1px solid var(--border);
  }
  
  .chat-messages {
      height: 350px;
  }
  
  .form-row {
      flex-direction: column;
  }
  
  .form-col {
      padding: 0;
  }
  
  .dashboard-header {
      flex-direction: column;
      align-items: flex-start;
  }
  
  .dashboard-header .btn {
      margin-top: 15px;
  }
}

/* Custom Loader */
.loader {
  display: flex;
  align-items: center;
  justify-content: center;
  margin: 20px 0;
}

.loader .dot {
  width: 10px;
  height: 10px;
  margin: 0 5px;
  border-radius: 50%;
  background-color: var(--primary);
  animation: dot-pulse 1.5s infinite ease-in-out;
}

.loader .dot:nth-child(2) {
  animation-delay: 0.2s;
}

.loader .dot:nth-child(3) {
  animation-delay: 0.4s;
}

@keyframes dot-pulse {
  0%, 100% { transform: scale(0.8); opacity: 0.5; }
  50% { transform: scale(1.2); opacity: 1; }
}

/* Notification Dropdown */
.notifications-dropdown {
  position: absolute;
  top: 40px;
  right: -10px;
  background-color: white;
  border-radius: var(--border-radius);
  box-shadow: var(--shadow-lg);
  width: 300px;
  z-index: 1000;
  transform-origin: top right;
  transform: scale(0);
  opacity: 0;
  transition: all 0.2s ease;
}

.notifications-dropdown.active {
  transform: scale(1);
  opacity: 1;
}

.notifications-header {
  padding: 15px;
  border-bottom: 1px solid var(--border);
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.notifications-list {
  max-height: 350px;
  overflow-y: auto;
}

.notification-item {
  padding: 15px;
  border-bottom: 1px solid var(--border);
  transition: var(--transition);
}

.notification-item:hover {
  background-color: var(--light);
}

.notification-item.unread {
  border-left: 4px solid var(--primary);
  background-color: rgba(0, 86, 179, 0.05);
}

.notification-title {
  font-weight: 500;
  margin-bottom: 5px;
}

.notification-time {
  font-size: 0.8rem;
  color: var(--gray);
}

.notifications-footer {
  padding: 15px;
  text-align: center;
  border-top: 1px solid var(--border);
}

/* Animation */
@keyframes pulse {
  0% { box-shadow: 0 0 0 0 rgba(230, 57, 70, 0.4); }
  70% { box-shadow: 0 0 0 10px rgba(230, 57, 70, 0); }
  100% { box-shadow: 0 0 0 0 rgba(230, 57, 70, 0); }
}

.pulse {
  animation: pulse 2s infinite;
}
