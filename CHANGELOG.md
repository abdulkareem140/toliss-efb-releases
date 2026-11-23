# Changelog

Each version has a one-line summary (used for the Discord announcements and the release list)
followed by the details.

## 1.9.11 - 2026-11-23 - AOC messages on the MCDU, callsign from SimBrief
- AOC messages from the tablet (gate, delay answers, weather...) also go to the aircraft: they show on the MCDU, ATSU > AOC > REC MSGS, while the ToLiSS ATSU is online on Hoppie
- New setting: Send AOC messages to the aircraft (on by default)
- The ACARS callsign comes from SimBrief by itself: airline code + flight number, the same as the MCDU FLT NBR

## 1.9.10 - 2026-11-23 - Smooth door progress, aircraft ATSU status
- Doors that move in steps (the bulk door) show "Moving" smoothly up to 100% instead of flicking between Moving and Open
- AOC: when shared with the aircraft, a light shows whether the ToLiSS ATSU is logged on to Hoppie as your callsign, with what to check if it isn't

## 1.9.9 - 2026-11-22 - Aircraft states closer to ToLiSS
- Cold + dark also switches all six fuel pumps and the crew oxygen supply off
- External power, ADIRU + APU, Engines running and the engine start tiles switch the fuel pumps (and crew oxygen) back on first
- ADIRU + APU and Engines running switch EXT PWR off once the APU powers the aircraft

## 1.9.8 - 2026-11-21 - Start the aircraft from the tablet, BULK door fixed
- Ground Ops > Startup works from the tablet, no ISCS: ENG 1 / ENG 2 start, APU start, ADIRS align and the aircraft states (engines running, ADIRU + APU, external power, cold + dark)
- The tablet works ToLiSS's own cockpit switches step by step (batteries, ADIRS, APU master and start, bleed, beacon, engine mode, masters), waits for APU AVAIL and each engine, and shows the step it is on, with Cancel
- New ADIRS light (how many IRs are in NAV)
- BULK door: follows the real door position (A320neo: its own value) and tries each way to open it until the door moves; no more "did not open" warning

## 1.9.7 - 2026-11-21 - Startup page, new map, real CPDLC and telex
- Ground Ops > Startup: live engine and APU gauges, power lights, the start sequence, quick starts and aircraft states (found on the aircraft by name, else they open the ISCS)
- Ground Ops redesigned: door and service tiles; the BULK door works; no more false "door didn't move" warnings
- Map: light chart by day, glowing route, airliner symbol with a 2-minute track line, new info card with progress, scale bar and north arrow
- AOC: messages look like real ACARS printouts; real telex and CPDLC from Hoppie's ACARS network arrive in the inbox (Airline > Website > ACARS NETWORK); send telex to any station

## 1.9.6 - 2026-11-21 - AviTab option removed
- Removed "Draw in the ToLiSS AviTab area": fit the EFB on the tablet's own screen with Fit on the tablet instead

## 1.9.5 - 2026-11-21 - Fit the EFB right on the tablet
- Edit mode on the 3D tablet: drag the corners or edges to the screen's edges, the middle to move it, ROTATE, DONE - the EFB fills it edge to edge
- Start it from Settings > Cockpit > Fit on the tablet, or Plugins > ToLiSS EFB > Fit cockpit tablet
- A new aircraft type starts in this mode: click the middle of the screen, then drag

## 1.9.4 - 2026-11-21 - Exact resizing on the cockpit tablet
- The EFB fills the calibrated area corner to corner: Narrower / Wider and Shorter / Taller each change exactly by the step (it used to keep the iPad's shape, so some presses did nothing and then it jumped)
- Finer steps: 0.5, 2, 8 and 32 texture pixels; the exact size is shown
- The AviTab button is now "Draw in the ToLiSS AviTab area", says it's only for the tablet's AviTab page, and has "Back to my calibration"

## 1.9.3 - 2026-11-21 - Exact cockpit screen from AviTab.json, arrow keys
- Settings > Cockpit > Use the ToLiSS AviTab screen: the exact tablet area from the aircraft's AviTab.json (built in for every ToLiSS type)
- Fine tune: Up / Left / Down / Right laid out like arrow keys; resizing keeps the picture centred instead of sliding it
- Plugins > ToLiSS EFB: Show tablet, Open in its own window and Show on cockpit tablet show an on/off dot

## 1.9.2 - 2026-11-21 - Airport charts, and the ToLiSS vehicles explained
- Map: zoom in on an airport, or press ARPT, for its chart: aprons, taxiways with names, runways with numbers, stands
- Far-away airports are drawn smaller so the map stays readable
- ToLiSS vehicles: ToLiSS lets only its ISCS call its stairs, catering trucks and belt loaders, so the tab now opens the ISCS (no more switches that couldn't work); old vehicle choices are forgotten

## 1.9.1 - 2026-11-21 - A clean start every time
- When X-Plane starts, the last flight is deleted, so no old flight shows up hours late. Turn on Settings > Keep the last flight when X-Plane starts to keep it

## 1.9.0 - 2026-11-21 - Update notice on the Home screen
- When a new version is waiting, a banner on the Home screen says so, with What's new (the release notes) and Later

## 0.9.0 - 2026-11-21 - The Map becomes an aviation chart
- Land and sea, coastlines, country borders, lakes and cities (Natural Earth, works offline)
- X-Plane's own airports, VORs, NDBs and airways, shown as you zoom in; APT / NAV / AWY buttons
- Your Navigraph data is used when it's in X-Plane's Custom Data folder

## 0.8.1 - 2026-11-21 - Map buttons, ToLiSS vehicles and doors
- Map: the + / - / ROUTE / PLANE buttons work; ROUTE shows the route even when the aircraft is parked far away
- ToLiSS vehicles: animation datarefs are no longer picked by themselves (they can't remove a vehicle)
- New Learn button (Ground Ops > Customize): switch the vehicle in the aircraft and the tablet finds its control
- A message when a door doesn't close (ToLiSS keeps a door open while stairs or a catering truck are at it)

## 0.8.0 - 2026-11-21 - Live ETA, landing calculator, map and logbook
- Live ETA after departure from where the aircraft is along the route: status bar, Home and AOC
- Landing calculator: VLS, VAPP and landing distance with MAX MAN, MED and LO braking, with a runway picture
- Map app with the route, top of descent, airports, your track and the aircraft
- Landing rate (ft/min, G, grade) after every touchdown, and a Logbook app that records every flight

## 0.7.2 - 2026-11-21 - Takeoff calculator like the ToLiSS one
- Same layout as the calculator in the ToLiSS tablet, in the Airbus cockpit font; values and labels stay in their own rows on the 3D cockpit tablet
- Same numbers as the ToLiSS calculator for the A320: CONF, FLEX, V1 range, VR, V2, THS and GREEN DOT
- Runway picture with the accelerate-stop distances and stop margins at V1 MIN and V1 MAX
- Wind, OAT and QNH from the sim's own weather at the aircraft; TOW and CG follow the aircraft until you compute

## 0.7.1 - 2026-11-21 - Downloads move to toliss-efb-releases
- Downloads, updates and bug reports now live at github.com/abdulkareem140/toliss-efb-releases
- SkunkCrafts Updater follows the new place by itself after this update

## 0.7.0 - 2026-11-21 - Updates through SkunkCrafts, bug reports, smarter takeoff calculator
- Updates through **SkunkCrafts Updater**; the tablet tells you when a new version is waiting
- **Report a bug** from the tablet (Settings > About), with diagnostics and your folder names removed
- Takeoff calculator finds airports by ICAO, IATA or X-Plane's old ID (OKKK/KWI), adds **GREEN DOT**, fills in the METAR by itself
- Removed the Web app and the 3D tablet model

## 0.6.2 - 2026-11-20 - Livery registration and MSN
- The tablet reads the livery's registration and MSN; tap it on Home to set your own per livery

## 0.6.1 - 2026-11-20 - Ground Ops Customize fixed
- Customize tested end to end in the window and on the 3D cockpit tablet

## 0.6.0 - 2026-11-20 - Talk to AOC, ToLiSS vehicles, new takeoff calculator
- Send AOC delay reports with IATA delay codes, in-range reports, requests, tech log, free text; AOC answers and sends its own messages
- Automatic OUT / OFF / ON / IN movement messages
- ToLiSS passenger stairs, catering trucks and baggage loaders in Ground Ops
- Takeoff calculator redrawn like an Airbus cockpit display, with a runway picture and windsock
- Departure clock follows the whole flight, to ON BLOCKS; CG shown

## 0.5.0 - 2026-11-20 - Looks like a real iPad
- Aluminium frame, iPadOS status bar, Home Screen widgets, app icons and a dock, frosted glass
- iPad frame on the 3D cockpit tablet

## 0.4.0 - 2026-11-20 - Real doors, cabin PA in your voice, AOC stands
- Real door layout for every ToLiSS type, including BULK
- Record cabin announcements with your own voice, muffled in the cockpit and clear in the cabin
- Departure countdown; AOC sends your arrival stand from X-Plane's airport data
- FlySmart-style takeoff calculator; auto calibration for all types

## 0.1.0 - 0.3.0 - 2026-11-19 - First versions
- SimBrief OFP, loadsheet with boarding, ground services and doors, weather, performance, checklists
- Floating, pop-out and VR window, and the 3D cockpit tablet with calibration
- Wallpapers including your own pictures, Levant VA website
