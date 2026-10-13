# WaterWise — VS Code prototype

## Run
1. Install Node.js LTS.
2. Extract this ZIP and open the folder in VS Code.
3. Open Terminal → New Terminal.
4. Run `npm install`.
5. Run `npm run dev`.
6. Open the localhost URL shown in the terminal (usually http://localhost:5173).

## Included
- Manager dashboard with water-flow chart and KPI cards
- Simulated leak alerts and incident workflow
- Assign technicians, update status, and add resolution notes
- Sensor status and location page
- Reports and CSV export
- Local browser persistence via localStorage
- Optional Supabase connection test and starter SQL schema

## Optional Supabase
1. Create a Supabase project and run `supabase/schema.sql` in SQL Editor.
2. Copy `.env.example` to `.env.local`.
3. Set `VITE_SUPABASE_URL` and `VITE_SUPABASE_ANON_KEY`.
4. Restart the dev server.

Important: this app currently stores its dashboard records in browser localStorage. Supabase connection testing is included, but all CRUD actions are not yet synchronized to PostgreSQL. The SQL schema is a starting point, not a production security policy. Add role-specific Row Level Security before deployment. Readings are simulated and detection is threshold-based; no real sensor or trained AI model is connected.
