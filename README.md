A2 Outdoor Services website starter

Open index.html in a browser.

Included:
- Services and pricing
- Complete $60 package
- Call/Text button using (325) 206-2463
- Instagram button for @a2outdoorservices
- Booking form
- Customer accounts and booking history
- Availability controls
- Admin booking/status panel
- Reviews
- Promo code storage
- FAQ
- Mobile responsive design

Important:
This is a front-end starter. Real online payments, secure customer accounts, real SMS notifications, and production admin security require a hosted backend plus payment/SMS services. Do not collect real card numbers in this demo.
A2 OUTDOOR SERVICES - SECURE OWNER LOGIN SETUP

This version removes the hard-coded PIN. The owner login uses Supabase Authentication and database Row Level Security.

IMPORTANT
Because A2 Outdoor Services is a minor-run business, have a parent/guardian help create and manage any third-party payment/authentication accounts if required by the provider's terms.

1. Create a Supabase project.
2. In Authentication > Users, create the owner's email/password account.
3. Open SQL Editor and run supabase_setup.sql.
4. Copy the owner's User UUID from Authentication > Users.
5. In the SQL file, uncomment the INSERT line and replace YOUR_OWNER_USER_UUID with that UUID, then run it.
6. In Project Settings > API, copy the Project URL and the public anon/publishable key.
7. Open index.html and replace:
   YOUR_SUPABASE_URL
   YOUR_SUPABASE_ANON_KEY
   with those public values.
8. Upload the updated index.html to GitHub Pages.

SECURITY NOTES
- Never put the Supabase service_role/secret key in index.html.
- The anon/publishable key is designed to be public; Row Level Security is what protects database data.
- The five-tap trigger only hides the login UI. It is NOT the security boundary.
- The real security boundary is Supabase Authentication + owner_access RLS policies.
- The sample dashboard UI is ready for protected database operations, but the existing demo booking form is still only a front-end demo until it is connected to the protected bookings table.
