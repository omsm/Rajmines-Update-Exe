# CSM and RYM weighbridge systems

A plain comparison for internal circulation and for discussion with the Department.

This note answers three questions. What does the CSM system actually do. What does the RYM Grenergy deck actually propose. And why handing the gate to a camera, and trusting the picture of a truck, makes illegal trips easier rather than harder.

The RYM material referred to here is their deck “RYM Weighbridge AI PPT” (3 October 2026).

---

## 1. The short version

CSM decides a trip from things a video cannot invent: a sensor that physically sees the truck, a weighing instrument that physically feels the load, and a tag read at the bridge. Cameras are already part of CSM. They record the front, the load, and the weighing display. They do not decide that a truck has entered, and they do not decide the royalty weight.

RYM’s slides say two different things. In one model they keep CSM and add a camera dashboard that flags suspicious trips after the pass has been issued. In the other model they still keep RFID, GPS, and the same weighing machine, and add cameras on top. A yard that runs on cameras alone is a third idea. It is the weakest of the three, and it is the one that opens new ways to fake a trip.

The magnetic-plate case does not prove that cameras should replace the present system. The person at the weighbridge fitted a matching number plate and showed the matching RFID tag. Plate text and tag text agreed. Slide 8 of the RYM deck proposes that same plate-plus-RFID check as their remedy. The check they are offering is the check that was already satisfied.

---

## 2. What the CSM system is

CSM is the automation that runs the weighbridge and talks to e-Rawanna. A trip is allowed only when the physical events happen in order. If the order breaks, the software returns to idle and no pass is generated.

Hardware on the bridge:

| Item | What it does in ordinary language |
| --- | --- |
| Three sensors (entry, weighbridge, exit) | Each sensor is ON when a vehicle is in front of it, and OFF when the road is clear. They are physical. Light, dust, and a video do not change them. |
| Weighing instrument (digitizer) | The legal scale. It reports the kilograms on the platform. |
| RFID reader | Reads the vehicle tag through a direct connection to the software. The tag is checked with the server. |
| Front camera | Reads the number plate and records the truck. |
| Top camera | Records what the truck is carrying. |
| Digitizer camera | Records the weight shown on the weighing machine, from the cabin. |
| Display, signal, barrier, announcement | Optional. They tell the driver what to do. They do not create the pass. |
| Controller | Connects the sensors, lights, and barrier to the software. |

Cameras are already there. They are the evidence of the trip. They are not the switch that starts it.

### How a genuine trip has to unfold

1. **Bridge empty.** The scale reads zero and all three sensors are OFF. That is “no vehicle on the weighbridge.”
2. **A new trip starts only at the entry sensor.** The entry sensor turns ON, the scale is still zero, and the weighbridge and exit sensors are still OFF.
3. **While the truck is coming on, and before it is sitting on the weighbridge sensor alone,** the weight is watched. If the weight falls back to zero, the trip resets. If the weight falls below 40 percent of the highest weight already reached on that approach, the trip resets. A truck that rolls off, or a weight that collapses halfway, does not continue. The “more than 5 tonne” rule is not applied in this stage. A truck still climbing onto the platform is not yet a full gross.
4. **Only when the truck is properly placed** — entry sensor OFF, weighbridge sensor ON, exit sensor OFF — does the next check start. The weight must stay above 5 tonnes, and the same weight must repeat until it is stable. If that does not happen, the trip resets. A person, a two-wheeler, or a truck parked half off the platform does not get a pass.
5. **The tag is read and the plate is read.** The truck number from the RFID must match the truck number from the plate. If they do not match, the mismatch is announced and the trip resets.
6. **The stable weight is sent to the server.** If it is inside the allowed range, the trip can proceed. If it is over or under, the operator is asked to confirm the weight on the display. If the operator does not confirm it, the trip fails.
7. **The three cameras save their pictures** with that trip: front, load, and the weighing display.
8. **The transit pass is generated, and the truck is asked to leave.** The next gross for that vehicle waits until this one is finished and the bridge is empty again.

That is several independent facts, all of which have to be true. A picture of a truck is only one of them, and it is not the one that opens the gate.

---

## 3. What the RYM system is

RYM describes itself as an AI surveillance layer for mineral movement. The deck is a set of slides, not a working description of a weighbridge cycle. Across those slides, three different systems are mixed together.

| What they are describing | What it actually is |
| --- | --- |
| **Model A, “add AI to CSM”** (their slide 12) | CSM and e-Rawanna stay. Cameras and a dashboard are added. Suspicious trips are flagged. The pass is still created by the existing system. An alert does not cancel a pass that has already been issued. |
| **Model B, “replacement”** (their slide 12) | They still show RFID, GPS, the weighing machine, plate reading, and e-Rawanna. Cameras are added for positioning and for watching the truck. This is not a camera-only weighbridge. |
| **The camera-only idea being argued in the meeting** | Sensors, the RFID reader, and the controller come out. Cameras decide that a truck has entered, where it is standing, and which truck it is. The weighing machine stays, because a camera cannot weigh a truck. |

Their own slide 10 calls the product an “AI surveillance layer for existing weighbridge infrastructure.” Their own slide 8 still ticks “ANPR + RFID check.” Their own slide 9 still draws the weighbridge, the tag, GPS, and the transaction next to the cameras.

So the honest comparison is:

- CSM is the system that **allows or refuses** the trip.
- RYM, on their own slides, is a system that **watches and comments** on the trip.
- A camera-only gate would **guess** the trip from a picture, and would still depend on the same weighing machine.

---

## 4. Side-by-side

| Question | CSM | RYM, as the deck describes it | If everything is left to the camera |
| --- | --- | --- | --- |
| How does the system know a truck has entered? | The entry sensor turns ON, and the scale is still at zero. | A camera zone decides that a truck shape is in the picture. | A video of a truck is enough, including a video that is not live. |
| How does it know the truck is properly on the bridge? | Only the middle sensor is ON. Entry and exit are OFF. | A drawn box on the camera view. | The box can be fooled by angle, shadow, a second vehicle, or a shifted pole. |
| How is the weight taken? | From the weighing instrument, and only after the weight has settled above 5 tonnes. | From the same weighing instrument. Their “AI weight” on slide 8 is a second look at the display (they show 16.70 and 16.72). | The camera photographs the number. It does not weigh the load. If the display is wrong, the photograph is wrong with it. |
| How is the truck identified? | RFID, then the plate, and the two must match. The server accepts the tag. | Slide 8 proposes the same pairing: plate reading plus RFID. | The plate in the picture is accepted. A magnetic plate, a borrowed plate, or a clear print of a plate satisfies it. |
| What stops a second pass for the same weighing? | The trip has to finish, the truck has to leave, and the scale has to return to empty before another gross is allowed. | Their slides show the repeats **after** the passes exist, and mark them “duplicate.” | A looped video of the same truck, plus the same weight, can be presented again. |
| What happens in dust, night, glare, or rain? | Sensors and the scale still work. A poor plate photo does not, by itself, create a pass. | Plate reading and position detection both drop. | The site falls back to a person. That person is the same role that arranged the magnetic-plate trips. |
| What is kept as proof? | Sensor order, weight readings, tag, and the three photos, stored with the trip. | Photos, a dashboard, and an alert. | If the camera is the proof and the camera was shown a recording, the proof is the recording. |
| What does the Department get if the system fails? | The trip does not complete. No pass. | A row on a dashboard, often after the pass is already out. | Either a fake trip that looks normal, or an honest trip that cannot be completed until someone overrides it. |

---

## 5. Their slides, set against what CSM already does

The deck’s title on one slide is “Catastrophic Breakdown of CSM Weighbridge Automation Software.” The points below are the charges on that slide and on the following “how we solve it” slide. Each one is something CSM already treats, or something their own remedy repeats.

### 5.1 “Too much dependence on hardware”

**Their point.** Sensors, a reader, and a controller are a weakness.

**What we do.** Those devices are the part of the system that cannot be satisfied by a picture. The weighing platform, the load cells, and the indicator stay in their design too. They are not proposing to remove the weighing instrument. They are proposing to remove the devices that check the vehicle is really there, and to keep the device that produces the royalty weight.

**Why this does not help.** A mineral yard is dust, night, sun, and mud. Hardware that touches the truck is more reliable there than a lens. Dependence on a sensor is a choice to fail safe: if the sensor pattern is wrong, there is no pass.

### 5.2 “Sensors can be manipulated”

**Their point.** Someone can block or bypass a sensor. Their answer on slide 8 is “tamper detection” by camera, and “AI vehicle positioning” instead of the sensors.

**What we do.** One sensor turning ON is not a trip. The truck must arrive at the entry, come fully onto the middle sensor, keep a real weight while it does so, settle above 5 tonnes, and later leave. If someone holds a sensor or blocks it, the pattern fails and the software resets. A blocked sensor cancels the trip. It does not invent a successful one.

**Why a camera is the easier thing to manipulate.** A sensor has to be physically occupied. A camera zone can be satisfied by a recording, by a printed picture, by a person standing in the frame, by a shadow, or by moving the camera a few degrees so that the yard entrance always looks “occupied.” Their slide calls sensor presence an incomplete proof, and then replaces it with a weaker presence test.

### 5.3 “GPS can fail or be faked”

**Their point.** Location data can be wrong. Their answer is “GPS validation.”

**What we do.** At the weighbridge, the question is whether this truck is on this platform. The entry sensor, the middle sensor, and the scale answer that. GPS matters on the road, between mines and destination. It is not what allows the weighing.

**Why their answer conflicts with their own slide.** The next slide says GPS can be weak or spoofed. Model B still shows GPS as one of the ticks. A yard camera does not fix a lie about a route ten kilometres away.

### 5.4 “The same vehicle, many rawannas”

**Their point.** They show one truck, one weight, many e-Rawanna numbers in a few minutes. The example used through the opening slides is vehicle RJ47GA5509, 20.12 tonnes, several passes within about thirteen minutes on 25 September 2026, with a claim of about twenty rawannas. They also show large “suspicious” and “confirmed leakage” tonnages for Jaipur, Jodhpur, and Sojat.

**What we do.** A second gross is a new trip. It is legal only after the previous truck has left and the scale is empty again, and after a new entry has started. The same kilograms, three minutes apart, without the scale returning to zero, is not a second dispatch. A loaded tipper cannot unload and reload to the same ten kilograms in that time. The server can refuse that second pass from the facts it already has.

**What their slides actually show.** They show passes that were **already generated**, then mark them “REPEAT” and “Duplicate Trip.” That is a review after the event. Model A says the existing CSM workflow is preserved and an exception dashboard is added. A dashboard row does not pull back a pass that e-Rawanna has already confirmed.

**A counting caution.** A normal dispatch carries Royalty 1 and Royalty 2. Those are two numbers for one legal trip. Any report that treats that pair as two leakages is overstating the problem. The Department should ask, for each red number in the deck, whether Royalty 1 and Royalty 2 were counted as two incidents.

### 5.5 “Weight can be manipulated”

**Their point.** Slide 8 shows a display reading 16.70 tonnes and an “AI” reading of 16.72 tonnes, with a green tick.

**What we do.** The royalty weight is the weighing instrument, after the truck is on the middle sensor alone, the weight is above 5 tonnes, and the same reading has repeated. Every reading from the instrument is already recorded. The cabin camera photographs that display at the time of the trip, so a later dispute can see what the machine showed.

**Why 16.72 does not check 16.70.** Those two numbers are the same display, read twice. If someone tampers with the indicator, the camera and the “AI weight” both see the tampered number. Agreement between them means they looked at the same glass. It is not a second weighing. The legal weight remains the approved scale. Their own slides do not replace the load cells.

### 5.6 “Not enough visual check”

**Their point.** One look at a number plate is not continuous proof of identity. Their answer is more cameras, continuous video, and alerts.

**What we do.** Three cameras already cover the front of the truck, the material on top, and the weighing display. Those images are part of the trip record. What they are not asked to do is to replace the sensor and the scale.

**The limit of “more video.”** Video is useful when someone later asks “who was on the bridge.” Video is a poor guard when the person at the site is willing to show the camera whatever it expects to see. More cameras increase the number of things that must be cleaned, aimed, lit, and kept online. They do not add a fact the site staff cannot stage.

### 5.7 Slide 8 proposes the same RFID and plate check that was already bypassed

This is the point to keep in front of the room.

**What happened.** Weighbridge staff understood the rule. They made number plates of real trucks and paired each plate with that truck’s RFID tag. The plate was magnetic, so it could be stuck on for the trip. The driver presented the matching tag. The camera read the plate. The plate matched the tag. The software did what it was designed to do, and the trip succeeded.

**What slide 8 offers as the fix.** Under “RFID / number plate issues,” the remedy drawn on the slide is “ANPR + RFID check.” That is plate reading plus the tag. It is the same comparison.

**Why the loophole survives their remedy.** The fraud did not happen because the camera failed to read the plate. It happened because both sides of the comparison were prepared in advance. A new camera, a new model, or a new vendor running that same comparison will pass the same prepared pair. Closing that hole means the tag has to be read by the fixed reader as a vehicle credential, the weight has to behave like a real arrival and a real departure, and a second pass has to wait for an empty scale. Another look at the magnetic plate does not do those things.

### 5.8 “One signal is not enough” — their slide 9

**Their point.** They say RFID is not the physical vehicle, a sensor is not full positioning, a weight is not proof that the vehicle moved, one plate read is not ongoing identity, and GPS can be faked. The slogan is that a transaction should not depend on one signal.

**Where we agree.** No single reading should create a pass. CSM already withholds the pass until the sensor order, the approach-weight rule, the 5 tonne stable gross, the tag, the plate match, and the server check have all succeeded.

**Where their conclusion does not follow.** The diagram on that slide adds cameras to the RFID, the scale, GPS, and e-Rawanna. It does not throw the physical checks away. A meeting proposal that removes the sensors and the reader, and leaves the camera, is one signal. It is the signal their own weather, light, and plate examples show to be the least reliable.

---

## 6. Why relying on the camera promotes illegality

A camera reports what is put in front of it. A sensor reports that something is physically in its path. A scale reports the load on the platform. When the pass depends on the picture, anyone who can supply the picture can supply the trip. The ways below are ordinary, not sophisticated.

1. **A recorded video, played as if it were live.** The camera feed can be shown a recording of a truck entering and standing on the bridge. On the ground, no vehicle has entered. The software, if it trusts the picture, starts a trip for a truck that is not there. The date and time burned into a recording are not a protection. They can be changed before the video is played. A sensor does not move for a recording. The scale does not gain 20 tonnes because a screen shows a truck.

2. **The same plate-and-tag pair their slide 8 wants to use.** Staff stick on a magnetic plate of a permitted truck and present that truck’s tag. The camera reads the plate. The RFID matches. This has already produced successful trips. Their deck recommends this check as the solution to “RFID / number plate issues.” Repeating the check repeats the opening.

3. **A plate that is not the truck.** A dirty, covered, damaged, borrowed, or printed plate is what the camera will read. If that reading is allowed to identify the trip, the mineral moves against the wrong vehicle, the wrong lease, or a vehicle that is allowed to carry when this one is not. CSM already treats a plate that does not match the tag as a failed trip. Making the plate the main identity removes that refusal.

4. **Night, dust, glare, rain, and a dirty lens.** These are normal at a lease weighbridge. Plate reading fails, and the position box fails, often together, because the same cameras do both jobs. The site then needs a manual exception so that honest trucks can leave. Every manual exception is a path around the rule. The person who uses that path is the person who arranged the magnetic plates. CSM’s sensors and scale do not need daylight to know that a truck is on the platform.

5. **A camera aimed a little off, on purpose or by accident.** Position in their design is a box drawn on the view. A shifted pole, a loose bracket, or a different truck body changes who is “inside” the box. Staff can aim a camera so that the gate, or a parked vehicle, is always inside it. After that, trucks can be weighed, or skipped, without the picture ever showing the truth. A middle sensor does not care where a pole was bolted.

6. **Something that is not a truck, accepted as a truck.** Headlights, a shadow, a person, a loader, or a second vehicle in the frame can be taken as the truck, or can hide the truck. False trips and stuck honest trips both push the weighbridge toward override. Override is where unrecorded mineral starts.

7. **The weighing display, photographed and called a check.** If the number on the indicator is forced, the camera records the forced number and the “AI weight” agrees with it. The illegal weight now has a picture attached, which makes it look better audited than a number with no photo. The photograph becomes cover, not a control. The cabin camera in CSM is stored so that the Department can see the display. It is not treated as a second scale, and it should not be.

8. **The same clip used for the next pass.** Their own case is one truck and one weight, repeated. If the gate is a picture plus a weight, the picture can be played again and the same weight sent again. Detecting the pattern the next morning, on a dashboard, does not stop the passes issued overnight. Refusal has to happen before e-Rawanna confirms the trip.

9. **One failed camera takes several controls down at once.** In their layout the same cameras are asked to recognise the truck, read the plate, and decide the position. One cut cable, one filled lens, or one switched-off recorder removes all three. The weighbridge either stops, which will not be accepted in production, or someone completes the trip by hand. A failed entry sensor in CSM stops the trip. It does not silently turn the other checks into a person’s word.

10. **Alerts create a habit of ignoring alerts.** Model A produces a list of suspicious trips. If the list is large, and their own Jaipur slide talks about hundreds of suspicious cases, staff learn to click past it. An illegal trip that looks like the other rows survives. A rule that refuses the second pass never depends on someone noticing a red row.

Taken together, the camera-only gate does not remove the person at the weighbridge. It gives that person a softer control, and a picture they can arrange, and then calls the result automated.

---

## 7. Pros and cons, from CSM’s side

This is our assessment. It is written so that a reader can see what we claim and what we do not claim.

### CSM

**Strengths**

- The trip starts only when the entry sensor and an empty scale agree. A video of an entry does not start it.
- While the truck is still coming on, a fall to zero or a fall below 40 percent of the highest weight already seen cancels the approach. The truck has to actually come onto the platform and stay there.
- The 5 tonne rule is applied only when the truck is on the weighbridge sensor alone. A person or a light vehicle cannot complete a mineral trip. A half-positioned truck cannot either.
- The weight used for royalty is the weighing instrument, which is the instrument the law already recognises.
- The plate has to match the RFID. A mismatch is announced and the trip ends.
- Front, top, and display cameras keep evidence of who came, what was carried, and what the display showed.
- If the pattern is wrong, the software goes back to idle. Wrong pattern means no pass, not a doubtful pass.
- Optional lights, a barrier, and announcements guide the driver. They are not a second way to create a trip.

**Limits, stated plainly**

- Sensors, the reader, and the controller have to be installed, powered, and maintained. That is real work. It is also the work that keeps the gate physical.
- A person can still interfere with a sensor. The protection is that a broken pattern cancels the trip. Site staff still have to leave the equipment intact, and tampering has to be visible in the log.
- Matching a plate to a tag is not, by itself, enough. The magnetic-plate case proved that, if both are supplied together. The weight rules, the fixed reader, the empty-scale rule, and the stored photos have to stand with that match. We should not describe the plate check as the whole security.
- If the weight is outside tolerance, an operator can be asked to confirm the display. That confirmation has to stay uncommon, has to be stored with the photos, and has to be visible to the Department. A quiet override is a hole in any system, including ours.
- Dust on a lens still spoils a photo. In CSM that spoils the evidence picture. It does not, by itself, authorise the tonnes.

### RYM

**What is fair to grant**

- Looking back across many passes, and pointing at the same vehicle and the same weight in a short time, is a useful audit. The Department should want that kind of review.
- Extra copies of the front and load images, kept where site staff cannot delete them, help an enquiry.
- A state dashboard can show the Department trips that deserve a question, provided someone defines what “suspicious” means and the count does not treat Royalty 1 and Royalty 2 as two frauds.

**What we do not accept**

- The deck calls the present automation a breakdown, then proposes, on slide 8, the same plate-and-RFID check the magnetic plate already passed.
- Model A does not stop the illegal pass. It reports it. Reporting a confirmed e-Rawanna is not the same as refusing it.
- Model B still needs the scale, and still draws the RFID reader. It is not a reason to scrap the sensors.
- An “AI weight” that matches the indicator to a decimal is not a second weighing.
- Positioning by camera zone will be wrong in the conditions of a real lease, and each wrong decision either blocks an honest truck or allows a truck that is not where the picture claims.
- “Thirteen sites” and “three thousand sites in four to five months,” and the command-centre figures on the slide, need a site list and a data extract before they are treated as results. A designed picture of a control room is not an operating record.
- Removing the sensors and the reader, and leaving the camera in charge, increases the ways a trip can be staged. Section 6 is that list. None of those ways move the middle sensor or put real tonnes on the scale.

---

## 8. What should stay, and what we should tighten

For the Department, the practical position is:

1. Keep one system that is allowed to create the pass: CSM with e-Rawanna.
2. Keep the three sensors, the RFID reader, the controller, and the weighing instrument. They are what a recording cannot satisfy.
3. Keep the three cameras as the record of the truck, the load, and the display. Store them with the trip, on a clock the weighbridge staff cannot change.
4. Keep the two weight rules in the order they belong. During the approach, zero or a drop below 40 percent of the peak resets the trip. Above 5 tonnes, and a stable reading, is required only after the weighbridge sensor alone is ON.
5. Refuse a second gross for the same vehicle until the first trip has ended and the scale is empty. That is the direct answer to the repeated-rawanna slides, and it refuses the pass instead of flagging it the next day.
6. Treat an operator’s confirmation of an out-of-range weight as an exception that the Department can see, not as a normal success.
7. If the Department wants an independent review of old passes, that review can sit beside this system. It should not become a second system that also issues trips, and it should not be a reason to switch the gate from the sensor to the camera.

---

## 9. Bottom line

CSM already uses cameras, RFID, plate reading, sensors, and the scale. RYM’s deck, where it is specific, mostly offers to watch that arrangement and to repeat the plate-and-tag check.

The illegal trip that has already been demonstrated was not a failure of the sensor. Staff showed the camera a plate, and showed the reader a tag, that had been chosen to agree. Their slide 8 makes that agreement the solution.

A system that instead believes a camera about whether a truck entered will accept a recording of an entry when the platform is empty. That is a fake trip with a clean picture. Fake trips are easier, not harder, when the picture is the proof.

The secure automation is the one that withholds the pass until the truck has physically arrived, physically loaded the scale, physically matched a tag the server accepts, and physically left. The cameras should show that this happened. They should not be what makes it true.
