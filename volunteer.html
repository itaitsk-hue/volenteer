// nav.js — shared navigation for all Meyter pages
// Include this script in every HTML page

const ADMIN_PASSWORD = 'admin123';
const SUPER_PASSWORD = 'super123';

// Page map: id -> { file, label, icon }
const PAGES = [
  { id: 'home',      file: 'index.html',     label: 'בית',      icon: 'home' },
  { id: 'volunteer', file: 'volunteer.html',  label: 'התנדבות',  icon: 'volunteer_activism' },
  { id: 'docs',      file: 'docs.html',       label: 'תיעוד',    icon: 'photo_camera' },
  { id: 'articles',  file: 'articles.html',   label: 'מאמרים',   icon: 'article' },
  { id: 'podcast',   file: 'podcast.html',    label: 'פודקאסט',  icon: 'podcasts' },
  { id: 'forms',     file: 'forms.html',      label: 'טפסים',    icon: 'assignment' },
];

function buildNav(activePage) {
  let desktopLinks = '';
  let mobileLinks = '';

  PAGES.forEach(({ id, file, label, icon }) => {
    const isActive = id === activePage;
    if (isActive) {
      desktopLinks += `<a class="text-[#1a73e8] font-semibold border-b-2 border-[#1a73e8] transition-colors duration-200" href="${file}">${label}</a>\n`;
      mobileLinks  += `<a class="flex flex-col items-center justify-center bg-[#1a73e8]/10 text-[#1a73e8] rounded-full px-4 py-1 scale-110" href="${file}">
        <span class="material-symbols-outlined" style="font-variation-settings:'FILL' 1">${icon}</span>
        <span class="text-[11px] font-bold">${label}</span>
      </a>\n`;
    } else {
      desktopLinks += `<a class="text-slate-600 font-medium hover:text-[#1a73e8] transition-colors duration-200" href="${file}">${label}</a>\n`;
      mobileLinks  += `<a class="flex flex-col items-center justify-center text-slate-500" href="${file}">
        <span class="material-symbols-outlined">${icon}</span>
        <span class="text-[11px] font-bold">${label}</span>
      </a>\n`;
    }
  });

  const navHTML = `
  <!-- TopAppBar -->
  <header class="fixed top-0 w-full z-50 shadow-sm bg-[#f8f9fa]/80 backdrop-blur-xl">
    <nav class="flex items-center justify-between px-6 h-16 w-full max-w-screen-2xl mx-auto flex-row-reverse">
      <div class="flex items-center gap-3">
        <span class="material-symbols-outlined text-[#1a73e8] text-2xl">grid_view</span>
        <a href="index.html" class="text-2xl font-bold text-[#1a73e8] font-headline tracking-tight no-underline">מיתר גני תקווה</a>
      </div>
      <div class="hidden md:flex items-center gap-8 flex-row-reverse">
        ${desktopLinks}
      </div>
      <div class="flex items-center gap-2">
        <button onclick="goAdmin()" class="px-4 py-2 rounded-full bg-surface-container-high text-on-surface font-semibold text-sm active:scale-95 transition-transform">Admin</button>
        <button onclick="goSuper()" class="px-4 py-2 rounded-full bg-surface-container text-on-surface-variant font-semibold text-sm active:scale-95 transition-transform">⚙️</button>
      </div>
    </nav>
  </header>

  <!-- Mobile BottomNav -->
  <nav class="md:hidden fixed bottom-0 w-full z-50 rounded-t-[3rem] bg-white/90 backdrop-blur-lg shadow-2xl">
    <div class="flex justify-around items-center h-20 px-4 flex-row-reverse">
      ${mobileLinks}
      <a class="flex flex-col items-center justify-center text-slate-500" href="#" onclick="goAdmin();return false;">
        <span class="material-symbols-outlined">admin_panel_settings</span>
        <span class="text-[11px] font-bold">ניהול</span>
      </a>
    </div>
  </nav>

  <!-- Admin Login Modal -->
  <div id="adminLoginModal" style="display:none" class="fixed inset-0 bg-on-surface/40 backdrop-blur-md z-[200] flex items-center justify-center p-4">
    <div class="bg-surface-container-lowest rounded-xl p-8 w-full max-w-sm shadow-2xl">
      <h3 class="text-xl font-bold font-headline mb-2 text-center">🔐 כניסת Admin</h3>
      <p class="text-sm text-on-surface-variant text-center mb-6">הכנס סיסמה לגישה לממשק הניהול</p>
      <input type="password" id="adminPassInput" placeholder="סיסמה" 
        class="w-full px-4 py-3 rounded-xl bg-surface-container-high text-on-surface mb-3 text-right border-none outline-none"
        onkeydown="if(event.key==='Enter')checkAdminLogin()"/>
      <div id="adminLoginErr" class="text-red-600 text-sm text-center mb-3" style="display:none">סיסמה שגויה</div>
      <button onclick="checkAdminLogin()" class="w-full py-3 rounded-full bg-gradient-to-tr from-[#005bbf] to-[#1a73e8] text-white font-bold mb-2">כניסה</button>
      <button onclick="document.getElementById('adminLoginModal').style.display='none'" class="w-full py-2 rounded-full text-on-surface-variant text-sm">ביטול</button>
    </div>
  </div>

  <!-- Super Login Modal -->
  <div id="superLoginModal" style="display:none" class="fixed inset-0 bg-on-surface/40 backdrop-blur-md z-[200] flex items-center justify-center p-4">
    <div class="bg-surface-container-lowest rounded-xl p-8 w-full max-w-sm shadow-2xl">
      <h3 class="text-xl font-bold font-headline mb-2 text-center">⚙️ Super-User</h3>
      <p class="text-sm text-on-surface-variant text-center mb-6">גישה מוגבלת למנהל ראשי בלבד</p>
      <input type="password" id="superPassInput" placeholder="סיסמה"
        class="w-full px-4 py-3 rounded-xl bg-surface-container-high text-on-surface mb-3 text-right border-none outline-none"
        onkeydown="if(event.key==='Enter')checkSuperLogin()"/>
      <div id="superLoginErr" class="text-red-600 text-sm text-center mb-3" style="display:none">סיסמה שגויה</div>
      <button onclick="checkSuperLogin()" class="w-full py-3 rounded-full bg-gradient-to-tr from-[#005bbf] to-[#1a73e8] text-white font-bold mb-2">כניסה</button>
      <button onclick="document.getElementById('superLoginModal').style.display='none'" class="w-full py-2 rounded-full text-on-surface-variant text-sm">ביטול</button>
    </div>
  </div>`;

  document.getElementById('nav-root').innerHTML = navHTML;
}

function goAdmin() {
  if (sessionStorage.getItem('adminAuth') === 'true') {
    window.location.href = 'admin.html';
  } else {
    document.getElementById('adminLoginModal').style.display = 'flex';
    document.getElementById('adminPassInput').value = '';
    document.getElementById('adminLoginErr').style.display = 'none';
  }
}

function goSuper() {
  if (sessionStorage.getItem('superAuth') === 'true') {
    window.location.href = 'super.html';
  } else {
    document.getElementById('superLoginModal').style.display = 'flex';
    document.getElementById('superPassInput').value = '';
    document.getElementById('superLoginErr').style.display = 'none';
  }
}

function checkAdminLogin() {
  if (document.getElementById('adminPassInput').value === ADMIN_PASSWORD) {
    sessionStorage.setItem('adminAuth', 'true');
    document.getElementById('adminLoginModal').style.display = 'none';
    window.location.href = 'admin.html';
  } else {
    document.getElementById('adminLoginErr').style.display = 'block';
  }
}

function checkSuperLogin() {
  if (document.getElementById('superPassInput').value === SUPER_PASSWORD) {
    sessionStorage.setItem('superAuth', 'true');
    document.getElementById('superLoginModal').style.display = 'none';
    window.location.href = 'super.html';
  } else {
    document.getElementById('superLoginErr').style.display = 'block';
  }
}
