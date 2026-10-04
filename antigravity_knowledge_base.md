# OMNISIGHT DRONES — OMNI AI KNOWLEDGE BASE

> **How to read this document.** This is the source of truth for OMNI AI. Everything here comes from the "Project Omnisight" strategy / technical document (the PDF), except items tagged **[Website]**, which come from the specification cards and spec matrix published on the Omnisight website. All prices are in Indian Rupees (INR, ₹). Prices and financials are *conceptual estimates*.

---

## 1. Company / Platform Overview

* **Omnisight Drones** is a dual-market drone platform built on a **"shared core, divergent shell"** strategy (the PDF calls the programme **"Project Omnisight"**).
* One unified software and navigation "brain" powers two distinct hardware product lines:
  * **ARES** — a rugged, secure **tactical / defense** drone for military use.
  * **NOMAD** — an intuitive, lightweight **traveler / explorer** drone for civilians.
* The business is effectively **two businesses under one roof**: a consumer (traveler) business and a defense (military) business.
* Website tagline: **"Master the Air. Map the Ground."** **[Website]**
* Website positioning: a unified drone architecture using real-time SLAM, LiDAR topography and military-grade autonomy for tactical reconnaissance and exploration. **[Website]**
* Brand direction (PDF): a **design-first** brand — aerospace engineering combined with high-end industrial design. The tactical drone should look aggressive and stealthy; the software should feel like a high-end graphic design tool.
* Strategic thesis (PDF): to beat the large incumbents (e.g. DJI, Skydio) Omnisight does not need a better motor; it needs a vastly superior way for users to interact with the drone and the 3D data it collects.

---

## 2. Shared Omnisight Core Architecture

* Both drones share one core technology stack:
  * **Night-vision optics**
  * A built-in **3D scanner** (LiDAR or photogrammetry)
  * A **dual-navigation system** using both **GPS** and **visual/inertial odometry (SLAM)** for places where GPS is blocked or unavailable
* The same technologies are applied very differently in each model:

| Core capability | ARES (tactical) | NOMAD (civilian) |
|---|---|---|
| 3D environment scanner | High-resolution **LiDAR** | **Photogrammetry** |
| Night vision | Military-grade **infrared + thermal** imaging | Low-light **starlight sensors** (no heavy thermal camera) |
| GPS-denied navigation | Advanced **SLAM** + **encrypted inertial navigation** | **Optical-flow sensors** that track the ground |
| Build | Radar-absorbent materials, low-acoustic rotors, anti-jamming encrypted links | Foldable, lightweight (**under 250 g**), smartphone-app control with automated cinematic flight paths |

* **Omnisight Core on the website [Website]:** a dedicated on-edge neural processor that lets the aircraft map, decide and navigate completely **offline**, without relying on GPS constellations or cloud servers. Four published pillars:
  * **GPS-Denied Visual SLAM** — navigates dense forests, mountain ravines and jammed electronic-warfare zones using visual odometry and edge optical flow, with no external satellite lock.
  * **In-Flight 3D Mesh Engine** — generates OBJ and LAS point clouds mid-flight; rendered topographical meshes reach the ground station seconds before the aircraft lands.
  * **Zero-Trust Telemetry** — a hardware secure enclave provides end-to-end cryptographic control against signal hijacking, GPS spoofing and rogue takeovers.
  * **Open API & Hot-Swap Bay** — integrate gas sensors, multispectral cameras, searchlights or custom Python autonomous routes through an open SDK.

---

## 3. ARES — Tactical / Defense Drone

**Purpose (PDF):** designed for **forward reconnaissance, threat detection and covert operations**.

* **3D environment scanner:** high-resolution **LiDAR** that instantly generates topographical maps and detects anomalies in real time — for example camouflaged enemies, hidden bunkers or tripwires.
* **Night vision & thermal:** military-grade infrared and thermal imaging that can spot body heat through foliage or smoke.
* **GPS-denied navigation:** advanced **SLAM** plus encrypted inertial navigation. If an enemy jams the GPS signal, the drone keeps flying autonomously by reading the physical environment.
* **Build & security:** radar-absorbent materials, **low-acoustic rotors (silent flight)** and **anti-jamming encrypted communication links**.
* **Capabilities the PDF says a modern military-grade drone must have** (it "cannot simply be a commercial drone painted camouflage"; it must be engineered around survivability, secure data transmission and precision in hostile environments):
  * **GPS-denied navigation** — IMUs (position from acceleration and rotation) plus Visual SLAM (onboard cameras read the terrain and match it against pre-loaded maps).
  * **Secure, anti-jamming datalinks** — frequency hopping (the link rapidly switches frequencies several times per second) and military-grade encryption for video and telemetry.
  * **Advanced multi-spectral payloads** — EO/IR (high-resolution daytime camera combined with thermal imaging); laser target designators are listed as a general military-drone capability.
  * **Electronic-warfare (EW) hardening** — MIL-STD shielding against electromagnetic interference, radar jammers and directed-energy weapons.
  * **Low acoustic and thermal signatures** — acoustic dampening (special rotor blades and motors) and thermal masking (shielding battery and motor heat).
* **"Ghost Mode" autonomy (proposed feature):** if ARES detects that radio and GPS are being jammed, it switches to Ghost Mode — it reads the terrain with its cameras, matches it to a pre-loaded offline map and silently flies back to base on visual autopilot.
* **Published ARES specifications [Website]:**
  * Designation: OMNISIGHT-DEFENSE // MK-IV; marketed as **MIL-SPEC certified**
  * Starting price: **₹8,99,000**
  * Take-off weight: **6.4 kg** (exoskeleton armored)
  * Max flight endurance: **38 minutes** (dual Li-HV batteries)
  * Top airspeed: **140 km/h** (87 mph) dash
  * Payload: **4.2 kg**
  * Max range: **28 km**
  * Perception sensors: **FLIR Boson 640 thermal + 360° LiDAR**, plus a 640x512 night-vision pod
  * Data link: **AES-256** quantum-resistant encrypted telemetry with **frequency-hopping FHSS (900 MHz / 2.4 GHz)**
  * Airframe: carbon-titanium exo-frame rated **IP67** all-weather
  * Operating temperature: **-30 °C to +55 °C** (heated battery bay)
  * Edge processing: **dual NVIDIA Jetson Orin Industrial**
  * Described as able to map subterranean tunnels autonomously
* **ARES economics (PDF):**
  * Estimated manufacturing cost (COGS): **₹4,50,000 – ₹8,00,000 per unit**
  * Cost breakdown: mil-spec carbon-fiber frame (₹40,000), high-end thermal/IR camera payload (₹2,00,000+), high-resolution LiDAR scanner (₹1,40,000), encrypted anti-jamming radio link (₹1,20,000), hardened compute module for SLAM / GPS-denied flight (₹50,000), MIL-STD testing and assembly (₹60,000)
  * Suggested selling price: **₹8,00,000 – ₹13,00,000+** (starting price **₹8,99,000**)
  * Gross margin: **35% – 55%**
  * Software licence: **₹89,999 per year, per drone** (see section 16)
  * Industry context: tactical drones such as the FLIR Black Hornet or Skydio X2D can sell for tens of lakhs of rupees per unit, because the military pays for proprietary software and a secure supply chain, not just plastic and wires.

---

## 4. NOMAD — Traveler / Explorer Drone

**Purpose (PDF):** designed for **content creators, hikers and off-grid adventurers**.

* **3D environment scanner:** uses **photogrammetry** to map a hiking trail, a ruined castle or a campsite, so users can create **3D models of their travels** for virtual reality or social media.
* **Night vision:** **low-light starlight sensors** for nocturnal wildlife, stargazing, or navigating back to camp after dark — without relying on heavy thermal cameras.
* **GPS-denied navigation:** **optical-flow sensors** track the ground, so the drone can follow the traveler through dense forests or deep canyons where satellite signals cannot penetrate.
* **Build & interface:** **foldable and lightweight — under 250 grams** (to bypass strict aviation regulations in many countries), controlled through an intuitive **smartphone app** with **automated cinematic flight paths**.
* **Published NOMAD specifications [Website]:**
  * Designation: OMNISIGHT-CIVIL // MK-II; marketed as DGCA nano-class (under 250 g)
  * Starting price: **₹1,49,999**
  * Take-off weight: **249 g** (listed as no licence required)
  * Max flight endurance: **47 minutes** (high-density solid-state battery)
  * Top airspeed: **72 km/h** (45 mph)
  * Video: **8K RAW**
  * Perception sensors: **Sony 1-inch 8K starlight sensor (f/1.8)** plus dual stereo cameras
  * Data link: OcuSync dual-band Wi-Fi 7 with AES-128
  * Operating temperature: **-10 °C to +40 °C**
  * Edge processing: Omni-Micro Neural Engine (**60 TOPS**)
  * Features: onboard photogrammetry 3D-mesh generator; autonomous orbit, waypoint and cable-cam cinematic modes
  * Suggested uses: alpine expeditions, geological research and cinematographers mapping deep backcountry
* **NOMAD economics (PDF):**
  * Estimated manufacturing cost (COGS): **₹35,000 – ₹55,000 per unit**
  * Cost breakdown: lightweight carbon/plastic frame and standard brushless motors (₹6,000), lithium-ion battery (₹7,000), optical camera / starlight sensor (₹13,000), basic photogrammetry compute module (₹9,000), standard radio controller (₹6,000), packaging and assembly (₹9,000)
  * Suggested selling price: **₹1,25,000 – ₹1,75,000** (starting price **₹1,49,999**) — positioned as a premium "prosumer" tool, competitive with high-end travel and photography drones
  * Gross margin: **55% – 70%**
  * Net margin after marketing, retail/distributor cuts and customer support: typically around **10% – 15%**
  * Cloud subscription: **₹1,499 per month** (see section 16)

---

## 5. ARES vs NOMAD

* **Same brain, different shell:** both run the shared Omnisight Core (night vision + 3D scanning + GPS/SLAM dual navigation) but are built for opposite environments.

| Attribute | ARES | NOMAD |
|---|---|---|
| Market | Tactical / defense (military) | Civilian traveler / explorer / creator |
| Mission | Reconnaissance, threat detection, covert operations | Travel capture, exploration, 3D models of places, cinematic video |
| 3D scanning | High-resolution **LiDAR** | **Photogrammetry** |
| Night vision | Military infrared + **thermal** | **Starlight** low-light sensor (no thermal) |
| GPS-denied navigation | Advanced **SLAM** + encrypted inertial navigation | **Optical-flow** ground tracking |
| Communications | Encrypted, **anti-jamming** (frequency hopping, AES-256) | Smartphone app link |
| Build | Radar-absorbent materials, silent low-acoustic rotors, rugged IP67 exo-frame | Foldable, lightweight, under 250 g |
| Weight **[Website]** | 6.4 kg | 249 g |
| Endurance **[Website]** | 38 min | 47 min |
| Top speed **[Website]** | 140 km/h | 72 km/h |
| Operating temperature **[Website]** | -30 °C to +55 °C, heated battery bay | -10 °C to +40 °C |
| Starting price | **₹8,99,000** | **₹1,49,999** |
| Recurring software | ₹89,999 / year per drone | ₹1,499 / month |
| Gross margin | 35% – 55% | 55% – 70% |

* **Cold alpine conditions:** by the published spec matrix **[Website]**, ARES is rated to a colder limit (-30 °C, with a heated battery bay) than NOMAD (-10 °C). NOMAD is better suited to lightweight alpine mapping and expedition capture within its own range; no further cold-weather performance data is provided.
* **Do not treat them as identical hardware:** ARES is a survivability-oriented tactical platform; NOMAD is a portable creator/explorer platform.

---

## 6. LiDAR Technology

* **LiDAR** stands for **Light Detection and Ranging**: a remote-sensing method that creates digital **3D replicas of the real world**.
* Like radar, it sends out a **pulse** that is reflected back to the sensor when it bounces off a surface; the time taken to return measures distance.
* It has been a constant in surveyors' toolkits since the **1980s**. It began as the **Terrestrial Laser Scanner (TLS)**, an accurate static solution; **SLAM** later made it possible to map handheld, on vehicles or by drone.
* **A LiDAR drone** is any aerial drone with a LiDAR sensor mounted to it — either an attached handheld LiDAR device or a permanent feature of the drone (for example Flyability's Elios 3).
* **Strength with vegetation:** the laser penetrates gaps between foliage and can map the ground below, which makes LiDAR useful in dense-vegetation areas that are hard for other scanning methods.
* **ARES uses LiDAR** for topographical maps and for detecting anomalies such as camouflaged enemies, hidden bunkers and tripwires. **[Website]** ARES carries a 360° LiDAR.
* **Practical tips:**
  * **Altitude:** a drone does not need to fly close to the ground for accurate LiDAR data, but lower altitude gives a higher point-cloud density.
  * **Georeferencing:** SLAM does not need GPS, but reflective targets are an ideal way to obtain georeferenced data.

---

## 7. Photogrammetry

* In **photogrammetry**, a drone captures **many overlapping images** over the mapped area so that every point on the ground is visible from multiple angles and viewpoints.
* Those overlapping views provide the detail needed to build a **3D model**, including **elevation and shape**.
* **Compared with LiDAR:** photogrammetry is **less accurate**, but it gives a **richer visual of the area through colour**.
* **Combined approach:** a LiDAR drone using photogrammetry as well can produce a more complete, **coloured point cloud**.
* **NOMAD uses photogrammetry** to map hiking trails, ruined castles and campsites and turn them into shareable 3D models for VR or social media. **[Website]** NOMAD has an onboard photogrammetry 3D-mesh generator.
* The PDF's design principle for 3D output: a traveler who scans a ruin should get a smooth, animated, shareable 3D asset.

---

## 8. SLAM / GPS-Denied Navigation

* **SLAM = Simultaneous Localization and Mapping:** mapping an area while keeping track of the device's own location within it.
* SLAM **does not require satellites**, so it suits indoor and underground environments, and it lets users map underground, overground, or move seamlessly between the two. It makes mapping mines and caves possible.
* **Visual SLAM** has matured significantly in the last five years: drones can now navigate underground, indoors or in electronically jammed environments by "seeing" their surroundings.
* **Why it matters:** in modern warfare GPS is routinely **jammed or spoofed** by electronic-warfare systems, so a military drone must navigate without satellite guidance.
* **Building blocks:**
  * **IMUs (Inertial Measurement Units):** internal sensors that calculate position from acceleration and rotation.
  * **Visual SLAM:** onboard cameras read the terrain and match it against pre-loaded maps to hold course.
* **ARES:** advanced SLAM with encrypted inertial navigation; "Ghost Mode" is the proposed fallback that flies home on visual autopilot using a pre-loaded offline map when radio and GPS are jammed.
* **NOMAD:** **optical-flow sensors** track the ground so the drone can follow a traveler through dense forests and deep canyons where satellite signals cannot reach.
* **Dual navigation:** both drones combine GPS with visual/inertial odometry (SLAM).

---

## 9. Drone Mapping & 3D Scanning

* **Two scanning methods:** LiDAR (accurate, works through foliage, ARES) and photogrammetry (colour-rich, NOMAD). They can be combined for a coloured point cloud.
* **Flight patterns** (depend on terrain and mission):
  * **Grid** — ideal for capturing large areas and ensuring coverage.
  * **Round** — great for monuments or buildings, circling the object.
  * **Comb** — ensures good coverage in irregular environments and helps with loop closure.
* **Outputs [Website]:** OBJ and LAS point clouds generated mid-flight.
* **Visualization philosophy (PDF):** raw LiDAR or photogrammetry data is useless if it is hard to read. Omnisight's software should render scans beautifully — a traveler's scan becomes a smooth, shareable animated 3D asset, while a soldier's scan of a treeline highlights anomalies intuitively.
* **Why it matters:** the 3D scanning capability is the product's core feature and the basis of its higher-margin software business.

---

## 10. Use Cases

* **ARES (military / tactical):**
  * Forward reconnaissance and threat detection
  * Covert operations (silent flight, low acoustic and thermal signature)
  * Detecting camouflaged enemies, hidden bunkers and tripwires with LiDAR
  * Spotting body heat through foliage or smoke with thermal imaging
  * Flying in GPS-jammed airspace using SLAM
  * Mapping subterranean tunnels **[Website]**
  * Swarm roles: one drone as a secure high-altitude radio relay while another scans low to the ground
* **NOMAD (civilian / traveler):**
  * Content creators and hikers capturing cinematic video with automated flight paths
  * 3D models of trails, ruined castles and campsites for VR or social media
  * Nocturnal wildlife capture, stargazing and finding the way back to camp after dark (starlight sensor)
  * Following the traveler through dense forests and deep canyons without GPS
  * Alpine expeditions, geological research and backcountry mapping **[Website]**
  * Swarm roles: two drones in a synchronized orbit for multi-angle cinematic shots without a camera crew

---

## 11. Industry Applications

* **Where drone LiDAR surveying is used (PDF):**
  * **Mining** — capturing unforgiving environments to show progress.
  * **AEC (architecture, engineering, construction)** — repeatedly capturing sites from the air without disturbing work, to track change over time.
  * **Forestry** — dense-canopy capture for deforestation and carbon measurements.
  * **Heritage** — documenting historical sites and monuments with less invasive techniques.
  * **Disaster management** — mapping damage (including nuclear disasters) and understanding areas for search and rescue.
  * **Utilities** — repeat safe scans of powerlines and surroundings.
* **Third-party examples from the reference article** (these are *not* Omnisight products): Shamrock+ (handheld LiDAR mounted on a Freefly drone), Visualskies (scans for National Geographic's *Lost Cities*, including a jungle-covered lost city in Micronesia), CPE Tecnologia (3D mapping of Christ the Redeemer in Brazil), InspecDrone (using Flyability's Elios 3 to model a cement plant in Harburg, Germany). Drones that can carry a ZEB Horizon scanner include the DJI M300 (55 min flight time, up to 2.7 kg payload), the Freefly Alta 8 / 8 Pro / X (Alta X carries up to 35 lb) and Flyability's Elios 3.
* **Drone industry developments over the last five years (PDF):** autonomy and AI (machine-learning obstacle avoidance and subject tracking), matured GPS-denied Visual SLAM, military adoption and loitering munitions (notably in Ukraine, shifting focus to small, decentralized tactical quadcopters), and regulatory frameworks (remote ID and BVLOS certifications).
* **Market size (PDF, Fortune Business Insights, approximate INR equivalents):**

| Segment | 2025 valuation | 2026 projected | Growth |
|---|---|---|---|
| Total global drone market | ₹8.27 lakh crore | ₹9.07 lakh crore | ~9.6% CAGR |
| Military drone market | ₹1.78 lakh crore | ₹2.02 lakh crore | ~11.1% CAGR |
| Consumer drone market | ₹54,000 crore | ₹65,700 crore | ~14.1% CAGR |

  * More than 62 countries increased tactical drone procurement in 2025.
  * The global counter-drone market is projected to reach about ₹2.25 lakh crore by 2034.

---

## 12. Time-to-Data / Edge Processing

* **The problem:** normally a drone lands, the SD card is pulled, plugged into a heavy laptop, and software takes hours to render a 3D map.
* **Omnisight's answer — real-time edge rendering:** a compute module inside the drone processes the 3D photogrammetry or LiDAR data **during flight**. By the time the drone lands, a fully rendered, lightweight, web-ready 3D map has already been beamed to the user's smartphone or tactical tablet.
* **Positioning:** Omnisight aims to be the **fastest "time-to-data" / "time-to-insight"** drone on the market — solving the whole workflow, not just the aircraft.
* **[Website]:** the In-Flight 3D Mesh Engine delivers topographical meshes to the ground station seconds before landing; processing runs on dedicated edge hardware (dual NVIDIA Jetson Orin Industrial on ARES, 60-TOPS Omni-Micro Neural Engine on NOMAD).
* **Interface:** responsive web-based mission-control dashboards (JavaScript/HTML5) so a commander or production crew can watch the feed from any browser on any tablet, without complicated installs.

---

## 13. Open Architecture / Modular Payloads

* **Goal ("the Android of Drones"):** an airframe with **universal payload mounts** and an **open API**, in contrast to the closed "walled-garden" ecosystems of major brands (proprietary batteries, locked software, no custom sensors).
* **Examples from the PDF:** a military unit could attach a custom gas-leak sensor; a traveler could snap on a retro cinematic lens. Letting the community build hardware and software add-ons creates fierce brand loyalty.
* **[Website]:** the **Open API & Hot-Swap Bay** supports gas sensors, multispectral cameras, searchlights and custom Python autonomous routes via an open SDK.
* **ARES payload:** **[Website]** payload capacity is **4.2 kg**. Built-in sensing payloads are the high-resolution LiDAR scanner and thermal/IR (FLIR Boson) camera with a night-vision pod; additional sensors can be added through the open payload architecture. A complete list of approved ARES payloads is not provided.

---

## 14. Data Sovereignty / Privacy-by-Design

* **The market gap:** manufacturers such as DJI face bans or restrictions in the U.S., Europe and India over fears that flight logs and visual data are uploaded to foreign servers.
* **Omnisight's positioning:** verifiable **"Privacy-by-Design"** with an absolute **"air-gap" guarantee** — zero telemetry, video or 3D-mapping data touches the cloud **unless the user explicitly commands it**.
* **Why it matters:** strict data security, aligned with western military NDAA compliance standards, opens defense and infrastructure contracts that are legally closed to DJI products.
* **[Website]:** Zero-Trust Telemetry with a hardware secure enclave, and the ability to navigate and map completely offline.

---

## 15. Swarm / Multi-Drone Concepts

* **Concept ("Swarm UI"):** most drone interfaces are "one pilot, one drone"; Omnisight proposes swarm command software so **one operator can manage two or three drones at once**.
* **Military example:** one drone sits high in the sky as a secure radio relay while another flies low to do the 3D scanning.
* **Traveler example:** two drones fly a synchronized orbit around the traveler for complex multi-angle cinematic video without a camera crew.
* This is a proposed product direction in the strategy document.

---

## 16. Business / Subscription Model

* **Hardware + software:** hardware is becoming a low-margin commodity; the real profit comes from **software subscriptions (SaaS)**. The 3D scanning capability is the "golden ticket" to higher margins.

| | NOMAD (traveler) | ARES (military) |
|---|---|---|
| Hardware starting price | **₹1,49,999** | **₹8,99,000** |
| Recurring software | **₹1,499 / month** cloud subscription to process, render and store 3D terrain maps and cinematic videos | **₹89,999 / year** licensing fee per drone for proprietary AI threat-detection software and an encrypted fleet-management dashboard |
| Hardware gross margin | 55% – 70% | 35% – 55% |

* **Software margins** typically sit between **80% and 90%**.
* **Strategy highlights:**
  * Win on **software, UI and 3D visualization** — hardware is a commodity, but drone control software is often clunky and industrial.
  * Hyper-target the **"data handoff"** — be the "fastest time-to-data" drone.
  * Lean into a **design-first brand**.
  * Competitors named: DJI and Skydio (large incumbents); DJI dominates the consumer market.
* **Challenges for defense:** expensive certifications, smaller production batches, large R&D and compliance costs, and 2-to-3-year sales cycles before a first contract.

---

## 17. Known Product Limitations / Conceptual Constraints

* **Conceptual stage:** Omnisight, ARES and NOMAD are presented as a product concept. All prices, margins and financials are **conceptual estimates**, not confirmed retail offers.
* **Not covered by this knowledge base:** availability, ordering, delivery dates, warranty terms, official certifications, exact ARES camera resolutions, and approved accessory lists. For any of these, OMNI AI must say the information is not provided.
* **Technology trade-offs:**
  * Photogrammetry is **less accurate than LiDAR** (though it provides colour); LiDAR gives accuracy and works through foliage.
  * LiDAR point-cloud **density depends on flight altitude** (lower altitude, higher density).
  * SLAM does not require GPS but **georeferenced results need reflective targets**.
  * NOMAD uses a **starlight sensor, not thermal imaging**; thermal and LiDAR are ARES capabilities.
  * The PDF notes that prioritizing one subsystem in drone design affects the others, but gives no specific trade-off figures.
* **Regulation:** the sub-250 g class is intended to bypass strict aviation rules "in many countries"; rules differ by country, so users should check local regulations.
* **Margins:** consumer hardware has thin net margins (around 10% – 15% for NOMAD even with a 55% – 70% gross margin).
