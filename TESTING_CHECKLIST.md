# TESTING CHECKLIST - Admin Panel Features

**Date:** December 9, 2025  
**Tester:** System Administrator

---

## 🔐 AUTENTIKASI (Authentication)

### Login Flow
- [ ] Navigate to `/admin/login`
- [ ] Enter valid email & password
- [ ] Verify successful login redirect to dashboard
- [ ] Verify session cookie set
- [ ] Test invalid credentials → error message
- [ ] Test empty fields → validation error
- [ ] Test "Remember Me" checkbox (if enabled)

### Register Flow (if enabled)
- [ ] Navigate to `/admin/(auth)/register`
- [ ] Fill form with new email & password
- [ ] Verify confirmation → login redirect
- [ ] Test duplicate email → error message
- [ ] Test password mismatch → error message

### Logout
- [ ] Click logout button on dashboard
- [ ] Verify redirect to login page
- [ ] Verify session cleared
- [ ] Verify cannot access admin without re-login

### Forgot Password (if enabled)
- [ ] Navigate to forgot password
- [ ] Enter email
- [ ] Verify email sent
- [ ] Click reset link
- [ ] Enter new password
- [ ] Verify can login with new password

---

## 📊 DASHBOARD

### Page Load
- [ ] Dashboard loads without errors
- [ ] All statistics cards display
- [ ] Recent berita list shows (or empty state)
- [ ] Recent surat list shows (or empty state)
- [ ] Loading state works while fetching data

### Statistics Display
- [ ] Total Berita count correct
- [ ] Published Berita count correct
- [ ] Total Views sum correct
- [ ] Total Surat Templates correct
- [ ] Statistik Penduduk displays
- [ ] Luas Wilayah displays

### Quick Actions
- [ ] "Create New Berita" button → redirects to `/admin/berita/new`
- [ ] "Create New Surat" button → redirects to `/admin/surat/new`
- [ ] Sidebar navigation links work
- [ ] Breadcrumb navigation works

---

## 📰 BERITA (News Management)

### List View (`/admin/berita`)
- [ ] Page loads with table of berita
- [ ] Pagination works (if > 10 items)
- [ ] Status filter works (All/Published/Draft)
- [ ] Category filter works
- [ ] Search by title works
- [ ] Delete button shows confirmation dialog
- [ ] Confirmation dialog cancels properly
- [ ] Delete action removes item from list
- [ ] Refresh button reloads data

### Create New (`/admin/berita/new`)
- [ ] All form fields present:
  - [ ] Title field
  - [ ] Slug field (auto-populated)
  - [ ] Excerpt textarea
  - [ ] Content editor
  - [ ] Category dropdown
  - [ ] Status radio (Draft/Published)
  - [ ] Thumbnail upload
  - [ ] Publish date picker
- [ ] Slug auto-generates from title
- [ ] Thumbnail preview shows after upload
- [ ] Form validation works
- [ ] Save button creates new berita
- [ ] Success message shows
- [ ] Redirects to berita list OR edit page

### Edit (`/admin/berita/[id]`)
- [ ] Page loads with pre-filled form
- [ ] All fields editable
- [ ] Thumbnail can be replaced
- [ ] Changes saved properly
- [ ] Success message shows
- [ ] Can navigate back to list

---

## 📝 KONTEN DESA (Content Management)

### Profil Desa (`/admin/konten/profil`)
- [ ] Page loads with profil form
- [ ] Nama desa editable
- [ ] Kecamatan/Kabupaten/Provinsi editable
- [ ] Deskripsi textarea editable
- [ ] Visi textarea editable
- [ ] Misi textarea editable
- [ ] Kontak info editable (telepon, email, website)
- [ ] Kepala/Sekretaris desa editable
- [ ] Save button updates profil
- [ ] Success message shows

### Struktur Pemerintahan
- [ ] List shows all positions
- [ ] Add new button opens modal
- [ ] Modal form has fields: nama, jabatan, NIP, email, telepon
- [ ] Save dalam modal adds to list
- [ ] Edit button populates form
- [ ] Delete button removes from list
- [ ] Changes persist after save

### Sejarah (`/admin/konten/sejarah`)
- [ ] Sejarah text editable
- [ ] Rich text editor works (if implemented)
- [ ] Save updates sejarah
- [ ] Displays on public `/jelajahi/sejarah` page

### Penduduk (`/admin/konten/jelajahi/penduduk`)
- [ ] Page loads with statistik
- [ ] Penduduk numbers editable
- [ ] Demographic data fields work
- [ ] Save updates properly

### Potensi (`/admin/konten/potensi`)
- [ ] List shows potensi items
- [ ] Create new potensi works
- [ ] Edit potensi works
- [ ] Delete potensi works
- [ ] Image upload works
- [ ] Items display on public `/potensi` page

### Galeri (`/admin/konten/galeri`)
- [ ] Upload image works
- [ ] Preview shows after upload
- [ ] Judul editable
- [ ] Kategori selectable
- [ ] Featured toggle works
- [ ] Delete removes image
- [ ] Order/urutan editable
- [ ] Images display on public `/galeri` page

---

## 📄 SURAT (Templates)

### List View (`/admin/surat`)
- [ ] Page loads with surat templates
- [ ] Table shows name, category, downloads
- [ ] Pagination works
- [ ] Active/Inactive toggle works
- [ ] Delete button removes template
- [ ] Search works

### Create (`/admin/surat/new`)
- [ ] Form loads with fields:
  - [ ] Name input
  - [ ] Slug field
  - [ ] Category dropdown
  - [ ] Description textarea
  - [ ] File upload (PDF/DOCX)
  - [ ] Active checkbox
- [ ] File upload accepts correct formats
- [ ] Save creates new template
- [ ] Displays on public `/surat` page

### Edit (`/admin/surat/[id]`)
- [ ] Pre-filled form loads
- [ ] Can update all fields
- [ ] Can replace file
- [ ] Changes saved properly

---

## ⚙️ PENGATURAN (Settings)

### Hero Slides (`/admin/pengaturan/hero`)
- [ ] List shows all slides
- [ ] Upload new slide works
- [ ] Edit slide title/description works
- [ ] Reorder slides works
- [ ] Delete slide works
- [ ] Changes display on homepage

### Kontak (`/admin/pengaturan/kontak`)
- [ ] Telepon editable
- [ ] Email editable
- [ ] Alamat editable
- [ ] Website editable
- [ ] Social media links editable
- [ ] Changes display on public contact page

### Notifikasi (`/admin/pengaturan/notifikasi`)
- [ ] Email notification toggle works
- [ ] Alert preferences configurable
- [ ] Settings saved properly

### Admin Users (`/admin/pengaturan/admin`) - Super Admin Only
- [ ] List shows all admin users
- [ ] Create new admin opens form
- [ ] Form has: email, nama, password, role
- [ ] New admin can login with credentials
- [ ] Edit admin updates user
- [ ] Delete admin removes user
- [ ] Deactivate user prevents login
- [ ] Role assignment (Super Admin/Admin) works

---

## 📊 ACTIVITY LOG

### View Logs (`/admin/activity-log`)
- [ ] Page loads with activity log
- [ ] Log shows recent activities
- [ ] Each entry shows: user, action, entity, timestamp
- [ ] Filter by action type works
- [ ] Filter by user works
- [ ] Date range filter works
- [ ] Search works
- [ ] Pagination works
- [ ] Log timestamps accurate

---

## 💬 MESSAGES

### View Messages (`/admin/pesan`)
- [ ] List shows all messages
- [ ] Columns: from, email, subject, date, status
- [ ] Pagination works
- [ ] Search by subject/email works
- [ ] Click to view full message
- [ ] Mark as read/unread works
- [ ] Delete message works
- [ ] Reply button sends email (if configured)

---

## 🔒 SECURITY

### Access Control
- [ ] Cannot access `/admin/*` without login → redirects to login
- [ ] Invalid session → redirects to login
- [ ] Super Admin can access all pages
- [ ] Regular Admin cannot access user management
- [ ] API calls without auth token fail

### File Upload Security
- [ ] Only allowed file types accepted
- [ ] File size limit enforced
- [ ] Malicious files rejected
- [ ] Files stored securely

### Data Validation
- [ ] Required fields enforced
- [ ] Email format validated
- [ ] Slug format validated
- [ ] Empty submissions rejected

---

## 🎨 UI/UX

### Responsive Design
- [ ] Page loads on mobile (< 768px)
- [ ] Page loads on tablet (768px - 1024px)
- [ ] Page loads on desktop (> 1024px)
- [ ] Navigation sidebar responsive
- [ ] Tables scrollable on mobile
- [ ] Forms readable on mobile

### Visual Feedback
- [ ] Loading spinners show
- [ ] Success messages display
- [ ] Error messages clear
- [ ] Hover states work
- [ ] Active navigation highlighted
- [ ] Buttons disabled during loading

### Navigation
- [ ] Sidebar navigation complete
- [ ] Breadcrumbs work
- [ ] Back buttons work
- [ ] Links navigate correctly

---

## ⚡ PERFORMANCE

- [ ] Pages load within 3 seconds
- [ ] Images lazy load
- [ ] No console errors
- [ ] No memory leaks
- [ ] API responses fast (< 500ms)

---

## 🐛 ERROR HANDLING

### Network Errors
- [ ] Offline message shows
- [ ] Retry button works
- [ ] Graceful error messages

### Validation Errors
- [ ] Required field errors show
- [ ] Format validation errors show
- [ ] Duplicate key errors show

### Server Errors
- [ ] 500 error handled gracefully
- [ ] 404 error handled gracefully
- [ ] Timeout handled gracefully

---

## ✅ FINAL CHECKLIST

- [ ] All modules tested
- [ ] No critical bugs found
- [ ] All features working
- [ ] Security validated
- [ ] Performance acceptable
- [ ] UI responsive
- [ ] Error handling good
- [ ] Ready for production ✅

---

**Tester Name:** _________________  
**Date Completed:** _________________  
**Sign Off:** _________________
