# 📸 **Next.js Gallery Application with Supabase**

A **modern, mobile-first, flat-design, SEO-optimized gallery application** built with **Next.js 14**, **Supabase**, **TailwindCSS**, and **Framer Motion**. The app is designed to efficiently organize, tag, and filter images across **Galleries**, **Albums**, **Cases**, and **Images**.

---

## 🚀 **Features**

✅ **Mobile-First Design:** Optimized for seamless responsiveness.  
✅ **Flat & Modern UI:** Built with TailwindCSS for clean, minimal styling.  
✅ **SEO Optimized:** Includes meta tags, sitemap, and structured data.  
✅ **Dynamic Image Organization:** Galleries → Albums → Cases → Images.  
✅ **Image Tagging & Filtering:** Support for advanced tag-based filtering.  
✅ **Multiple Image Upload:** Upload multiple images in bulk.  
✅ **Admin Dashboard:** Manage Galleries, Albums, Cases, and Images.  
✅ **Fast Load Times:** Leveraging Vercel Image Optimization and caching.  
✅ **Secure Auth System:** Powered by Supabase Authentication.

---

## 🛠️ **Tech Stack**

### **Frontend:**
- **Framework:** Next.js 14 (App Router)
- **Styling:** TailwindCSS + Radix UI Components
- **Animations:** Framer Motion
- **SEO:** Next.js Metadata API
- **Image Optimization:** Vercel Image Optimization

### **Backend / Database:**
- **CMS & Database:** Supabase
- **Auth:** Supabase Auth (Admin Access)

### **Deployment:**
- **Platform:** Vercel
- **CDN:** Cloudflare R2 (optional for storage optimization)

---

## 📂 **Project Structure**

```plaintext
/app
  ├── layout.tsx            # Global layout for the app
  ├── page.tsx              # Homepage (Galleries overview)
  ├── gallery/[id]/page.tsx # Displays albums for a selected gallery
  ├── album/[id]/page.tsx   # Displays cases for a selected album
  ├── case/[id]/page.tsx    # Displays images for a selected case
  ├── admin/page.tsx        # Admin dashboard for management
  ├── api/
      ├── galleries/route.ts # CRUD for Galleries
      ├── albums/route.ts    # CRUD for Albums
      ├── cases/route.ts     # CRUD for Cases
      ├── images/route.ts    # CRUD for Images
/components
  ├── Gallery/
      ├── GalleryGrid.tsx   # Displays all galleries
      ├── AlbumGrid.tsx     # Displays all albums in a gallery
      ├── CaseGrid.tsx      # Displays cases in an album
      ├── ImageGrid.tsx     # Displays images in a case
  ├── Admin/
      ├── ImageUploadForm.tsx # Upload multiple images
      ├── ImageManager.tsx    # Edit/Delete images
      ├── Filter.tsx          # Filtering UI
/lib
  ├── supabase.ts          # Supabase client configuration
  ├── imageUtils.ts        # Image optimization utilities
/public
  ├── images/              # Static placeholder images
.env.local                 # Environment variables
next.config.ts             # Next.js configuration
tailwind.config.ts         # TailwindCSS configuration
tsconfig.json              # TypeScript configuration
```

---

## 📊 **Database Schema**

### **1. Galleries**
- `id`: Unique identifier  
- `title`: Gallery name (e.g., Head & Neck, Breast, Body)  
- `description`: Description of the gallery  

### **2. Albums**
- `id`: Unique identifier  
- `gallery_id`: Reference to a gallery  
- `title`: Album name (e.g., Face, Nose, Breast Augmentation)  
- `description`: Description of the album  

### **3. Cases**
- `id`: Unique identifier  
- `album_id`: Reference to an album  
- `client_name`: Name or identifier of the client  
- `description`: Description of the procedure  
- `procedure_date`: Date of the procedure  
- `metadata`: JSON metadata (e.g., age, surgeon name, notes)  

### **4. Images**
- `id`: Unique identifier  
- `case_id`: Reference to a case  
- `image_url`: URL to the stored image  
- `caption`: Description or caption of the image  
- `tags`: Array of tags (e.g., `Before`, `After`, `Side View`)  

---

## 🔑 **Authentication**

1. Admin authentication via **Supabase Auth**.
2. Admin Dashboard is secured and requires login.
3. **Admin Features:**
   - Create/Edit/Delete Galleries
   - Add/Edit/Delete Albums
   - Manage Cases
   - Bulk Image Upload
   - Tag and Organize Images

---

## 🖥️ **How to Run Locally**

1. **Clone the Repository:**
   ```bash
   git clone https://github.com/your-repo/gallery-app.git
   cd gallery-app
   ```

2. **Install Dependencies:**
   ```bash
   npm install
   ```

3. **Set Environment Variables:**
   Create a `.env.local` file and add:
   ```env
   NEXT_PUBLIC_SUPABASE_URL=your_supabase_url
   NEXT_PUBLIC_SUPABASE_ANON_KEY=your_supabase_anon_key
   ```

4. **Start Development Server:**
   ```bash
   npm run dev
   ```

5. Visit [http://localhost:3000](http://localhost:3000) in your browser.

---

## 🚀 **Deployment**

1. Push code to **GitHub**.
2. Connect your repository to **Vercel**.
3. Add environment variables in **Vercel Dashboard**.
4. Deploy the project.

---

## 📜 **License**

This project is licensed under the **MIT License**.

---

## 📞 **Support**

- 📧 **Email:** support@yourdomain.com  
- 🌐 **Website:** [https://yourdomain.com](https://yourdomain.com)  

