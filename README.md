⚡ AAP — Electricity Bill Calculator
A modern, offline, single-file web app for calculating electricity bills onslab-based tariffs — built especially for Bangladeshi utility tariffs(lifeline / non-lifeline slabs, demand charge, meter rent, VAT).

No installation. No server. No accounts. Just open one HTML file.

HTML5JSOfflineDataLicense

✨ Features
🧮 Calculator
Slab-based billing — lifeline + non-lifeline slabs, charged from unit 1
Two input modes — enter units directly, or previous & current meter reading
Penalty toggle — one tap adds a configurable % (default 5%) of the total bill
Previous due / advance — carry arrears (positive) or advance (negative)
Demand charge modes — flat Tk, or per-kW of sanctioned load
Full breakdown — slab-wise table, energy, demand, meter rent, VAT, penalty,rounding adjustment, effective rate (Tk/unit) + an animated cost-composition bar
Insights — cost of the next unit, how far you are from the next slab,lifeline-cliff warnings, and month-over-month comparison
Reverse calculator — "I can pay Tk 2,000" → ≈ how many units
🛠️ Estimator
Appliance list — watt × hours/day × quantity → predicted units & billper appliance and combined; load the result into the calculator
Watt → Money — any load's cost per day / week / month / year
📈 History
Save bills by month; auto-fills "previous reading" from your last saved bill
12-month trend chart, per-entry delete, clear-all with Undo
⚙️ Tariff & Presets
Everything is editable — lifeline limit & rate, unlimited slabs, demand, meter rent, VAT %, penalty %
Save presets (e.g. DPDC 2024, Desco 2025) and switch with one click
Exact round-half-up final rounding (0.50 → 1) using integer paisa math— no floating-point surprises
🎨 Experience
Dark / light theme, smooth animations, fully responsive
100% offline — your data never leaves the browser (local Storage)
🚀 Getting Started
No build step:

Download index.html
Double-click it — done. Works on any modern browser (desktop & mobile).
Or run on GitHub Pages:

Push index.html and README.md to a repository
Repo → Settings → Pages → Source: main branch, / (root) → Save
Your app goes live at https://<username>.github.io/<repo-name>/
🧮 How the bill is calculated
Energy charge   = units priced through slabs (lifeline OR non-lifeline)Subtotal        = energy charge + demand charge + meter rent Total after VAT = subtotal × (1 + VAT%)With penalty    = total after VAT × (1 + penalty%)     [optional toggle]Payable         = round-half-up( With penalty ) + previous due − advance
Default tariff (editable): lifeline 1–50 @ Tk 4.63; slabs 1–75 @ 5.26,76–200 @ 7.20, 201–300 @ 7.59, 301–400 @ 8.02, 401–600 @ 12.67, 601+ @ 14.61;demand Tk 42, meter rent Tk 10, VAT 5%.

⚠️ Crossing 50 units loses the lifeline — all units are then re-priced through the non-lifeline slabs. Example (default tariff):

Units	Bill	Why
50	Tk 298	50 × 4.63 + 52, × 1.05
51	Tk 336	51 × 5.26 + 52, × 1.05
120	Tk 809	75×5.26 + 45×7.20 + 52, × 1.05
📸 Screenshots
Calculator	Estimator
Calculator	Estimator
🔒 Privacy
All data (tariffs, presets, history, estimator) is stored only in yourbrowser's localStorage. Nothing is uploaded, tracked, or synced.Clearing browser data removes it — export a backup if needed.

🧱 Tech
Single HTML file: HTML + CSS + vanilla JavaScript
Zero dependencies, zero build tools
All money math in integer paisa (Tk × 100) for exact rounding
🗺️ Roadmap
 Export / import data as JSON backup
 Print / PDF-friendly bill receipt
 Bangla (বাংলা) interface
 Multi-meter support
📄 License
Released under the MIT License.

⚠️ Disclaimer
AAP is an estimation tool. Actual bills may differ due to fuel-priceadjustments, rebate schemes, meter-specific charges, or tariff changes byyour utility. Always verify with your official bill.

3. Quick publish checklist
Rename your app file to index.html (required for GitHub Pages).
Create README.md with the content above.
Optional: add a LICENSE file (MIT — I can generate it with your name if you want).
Optional: add a screenshots/ folder with 2–3 captures (Calculator, Estimator, Tariff) and fix the paths — screenshots massively improve first impressions.
Fill the About description + topics on the repo page, then enable Pages (Settings → Pages → main / root).
