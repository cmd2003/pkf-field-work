# PKF Field Work

A first-person 3D audit simulation that runs in the browser. You sit at a desk in the client's office, read a sixteen-document client file, interview the CFO and the warehouse in-charge, write your own case notes, and stamp the year-end invoice **Passed** or **Adjustment Proposed**. A partner reviews your file at the end.

Built for PKF Sridhar & Santhanam training sessions. Single HTML file, no install, works on laptop and phone.

## Run it

Open `prototype/index.html` from a local web server (the page loads a few scripts from CDNs and works offline otherwise):

```bash
cd prototype && python3 -m http.server 8765
```

Then visit http://localhost:8765/. Chrome, Edge, Safari and Firefox on desktop and mobile are supported. Sound is synthesised in the browser.

The published version on claude.ai adds two things the local copy does not have: the two witnesses are driven by Claude, and the partner reads your typed notes and writes a review comment.

## What is in the case

*The March 31 Sale.* Zenith Components Ltd booked a ₹2.80 crore sale to Meridian Auto Systems on 31 March. Materiality is ₹42 lakh. The evidence is spread across the desk, a thirteen-document binder, and two people:

- Tax invoice, outward gate pass, and an email from the CFO on the desk
- Purchase order, sales register, customer confirmation, e-way bill, lorry receipt, count sheet, internal audit report, debtors ageing, bank covenant certificate, draft financial statements, board minutes, MCA extract with the CFO's related-party declaration, and last year's cut-off working paper in the binder
- Ramesh Menon, CFO, and Selvam K., warehouse in-charge, on the phone

Nine findings are hidden in the small print and the contradictions between witnesses. Offering tea or coffee changes how they talk to you.

## Controls

- Move the mouse to look, click to act. On phones, drag to look and tap to act.
- Click a paper to pick it up, the green binder or the "Client file" button to open the file, the phone to call a witness, the mug to drink.
- In the binder, click the right page to turn forward and the left page to go back. Scroll or press Z to zoom; the page pans under the cursor. Double-tap to zoom on phones.
- Type case notes in the panel on the left. The partner grades what you wrote.
- Pick up a stamp, then click the invoice.

## Structure

Everything is in `prototype/index.html`: scene, procedural textures, characters, documents, dialogue, scoring and sound. The rigged hand model is embedded in the page as base64 and also kept as `prototype/assets/hands.glb`.

Three.js r128 with post-processing passes is loaded from cdnjs and jsDelivr.

## Credits and licences

- Hand model: ["First Person hands rigged"](https://sketchfab.com/3d-models/first-person-hands-rigged-547a45535f0c4fe787948f7a7a6a88db) by David Fischer, licensed [CC BY 4.0](http://creativecommons.org/licenses/by/4.0/). Included unmodified as `prototype/assets/hands.glb` and embedded in the page.
- Fonts: Libre Caslon Text, IBM Plex Mono and IBM Plex Sans via Google Fonts (SIL Open Font License).
- Three.js: MIT.
- Everything else, including the case, documents, characters, textures and sounds, is generated in the page.

The company, people, documents and events in the case are fictional.
