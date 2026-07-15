MCD-01B-05 — Faux Wood Venetian Blinds
Status: Working Draft — Unverified (downgraded from self-declared "Approved Draft Baseline"; has not been through branch/review/Decision Register/verification process)
Version: v1.0 (pre-review)
Parent Document: MCD-01A — Sales MVP Product Engine Architecture
Reference Document: MCD-01B-04 — Wooden Venetian Blinds
Product Family: Standard Blinds

1. Purpose
This document defines the supplier-neutral product specification for Faux Wood Venetian Blinds within Solara OS.
It inherits the shared Venetian architecture established in MCD-01B-04 — Wooden Venetian Blinds and records only the genuine differences required for Faux Wood products.
Supplier-specific ranges, colours, dimensions, motorisation, pricing, manufacturing limitations and current availability remain within MCD-04 — Product Library & Supplier Management.

2. Product definition
A Faux Wood Venetian Blind is a made-to-measure internal blind comprising: a metal or reinforced headrail; horizontal synthetic slats designed to resemble painted or grained timber; ladder cord or decorative ladder tape; a matching synthetic bottom bar; a matching valance or pelmet; manual or supported motorised controls; installation brackets; applicable child-safety devices.
The product provides adjustable privacy and light control through slat tilting and can be fully raised using its lift system.

3. Product-family position
Standard Blinds -> Faux Wood Venetian Blinds
Faux Wood Venetian Blinds remain separate from: Wooden Venetian Blinds; Metal Venetian Blinds; Perfect Fit Venetian Blinds; shutters; exterior Venetian systems.
Perfect Fit Faux Wood Venetian Blinds are not included because no confirmed standard product currently exists.

4. Relationship to the Venetian reference implementation
This product inherits the following concepts from MCD-01B-04: Recess and Exact measurement; width and drop; slat size; ladder cord and decorative tape; manual tilt and lift controls; control-side arrangement; bracket allocation; valance or pelmet treatment; bottom bar; stack height; hold-down brackets; bay-window grouping; alignment; child-safety validation; motorisation eligibility; supplier-capability filtering; internal and customer-facing document rules.
This document overrides or extends the reference implementation only where Faux Wood behaves differently.

5. Design principles
Advisor-first; supplier-neutral; capability-driven; non-assumptive; technically safe; easy to reconfigure during a sales appointment.
The system must not assume that every Faux Wood range offers the same slat size, colour, tape, motorisation, maximum size, heat resistance, moisture suitability.

6. Material definition
Faux Wood Venetian slats are normally manufactured from PVC, synthetic polymer, composite polymer, or other supplier-defined moisture-resistant synthetic material.
The internal capability record must store the supplier's actual material description. The customer-facing product name remains "Faux Wood Venetian Blind" unless a specific material distinction is commercially useful.

7. Material behaviour
Faux Wood is generally more suitable than natural wood in rooms where moisture resistance is important. Typical benefits: resistance to normal household humidity; suitability for many kitchens; suitability for many bathrooms; consistent colour and grain; reduced natural variation; easier cleaning.
Faux Wood must not be described as indestructible or suitable for every environment. Behaviour may be affected by intense direct sunlight, heat build-up between glass and blind, poor ventilation, secondary coverings trapping heat, very dark slat colours, unusually large slat spans.

8. Moisture suitability
Recommendation Engine may recommend Faux Wood for bathrooms, kitchens, utility rooms, rooms with intermittent condensation, areas where natural wood may distort or absorb moisture.
System should not claim universal waterproofing unless supported by the selected supplier range. Advisor should still assess ventilation, direct water contact, persistent condensation, proximity to cookers/sinks/showers, warranty restrictions.

9. Heat and sunlight warning
Faux Wood slats may soften, twist or deform where excessive heat builds up. Survey and Recommendation Engines should warn where the window receives prolonged direct sunlight, the selected colour is dark, the glass has high solar gain, the blind will sit close to the glass, curtains or another covering may trap heat, ventilation behind the blind is limited.
Advisor may recommend a lighter colour, a real-wood alternative where appropriate, improved ventilation, leaving slats slightly open during extreme heat, another product type.

10. Core advisor workflow
Room; Window reference; Fit type; Width; Drop; Slat size; Colour and finish; Ladder cord or decorative tape; Tape width and colour; Manual or motorised operation; Control arrangement; Valance or pelmet; Brackets and extensions; Hold-down brackets; Installation height; Child-safety validation; Heat and moisture suitability; Supplier capability resolution; Price calculation; Survey confirmation.

11. Measurement mode
Faux Wood Venetian Blinds support Recess and Exact, following the same measurement architecture as Wooden Venetian Blinds. Supplier-specific recess deductions, manufacturing tolerances and finished sizes remain in MCD-04. The quotation must not display measurements or manufacturing deductions.

12. Slat size
Common Faux Wood slat sizes include 35mm, 38mm, 50mm, 63mm as illustrative examples of sizes that may exist across the supplier base — not a claim that all sizes are available on all ranges. The system must display only slat sizes supported by the selected supplier, range, colour, finish, operation type, width and drop.
A slat size may be restricted to one colour or finish; that restriction must be capability-driven.

13. Colour and finish
Possible Faux Wood finishes: smooth; fine grain; wood grain; embossed grain; flat matt; gloss; painted appearance; oak-style finish; dark contemporary finish.
Colour record must support: active; discontinued; temporarily unavailable; limited stock; legacy or remake only; supplier confirmation required.
Discontinued colours must not appear in the normal Product Builder. A supplier portal may continue to display discontinued colours for remaining stock, remakes or historic orders. Portal visibility alone must not reactivate them.

14. Colour-dependent capability
Colour can affect technical suitability. Capability model must support colour-specific rules including maximum width, maximum drop, direct-sunlight suitability, heat warning, slat-size eligibility, tape availability, painted slat ends, motorisation, current stock status.
A colour must therefore be treated as a technical capability object, not merely a decorative label.

15. Ladder construction
Supports ladder cord and decorative ladder tape. Availability must be filtered by supplier, range, slat size, colour, finish, width, drop, motorisation.
Known tape widths may include 19mm, 25mm, 38mm as illustrative examples. The system must not assume all tape widths are available across all Faux Wood ranges.

16. Tape selection
Product Builder may support matching tape, supplier-recommended tape, alternative coordinated tape, contrast tape, standard weave, decorative weave.
Capability record must include tape width, tape colour, slat compatibility, colour compatibility, surcharge, discontinued status. Where a matching tape has been discontinued with its blind colour, it must also be removed from standard quoting.

17. Manual controls
Manual Faux Wood Venetian operation includes tilt, raise and lower. Supported control arrangements may include standard split controls, reverse split controls, both controls left, both controls right, supplier-forced standard controls.
Some ranges permit only one standard arrangement. The system must apply range-specific control rules rather than copying Wooden Venetian control choices automatically.

18. Narrow-width controls
Some ranges may impose standard controls only, restricted same-side controls, no alternative control positions, minimum widths for selected arrangements. These rules belong in Supplier Capability. The Product Builder should automatically remove invalid arrangements rather than showing them and producing repeated errors.

19. Motorisation
Motorisation is optional and must never be assumed across the Faux Wood family. The shared Operation Engine supports Manual, Motorised — Tilt Only, Motorised — Tilt and Lift.
Current supplier evidence primarily supports tilt-only operation for selected Faux Wood ranges. Tilt-and-lift must remain hidden unless explicitly confirmed.

20. Motor eligibility
Motorisation must resolve using: Supplier + Range + Slat Size + Colour or Finish + Ladder Cord or Tape + Width + Drop + Area or Weight + Required Function + Power Type + Motor System.
System must support rules such as: 50mm only; selected colours only; ladder cord and tape both eligible; ladder cord only; tilt-only; minimum width; width/drop combination limits; battery or mains options; supplier-selected motor.

21. Unconfirmed motorisation
Where motor compatibility is not explicitly verified: Motorisation Availability: Not Confirmed / Advisor Visibility: Hidden / Quoting Status: Disabled.
The presence of a motor surcharge or motor component in a price list is not sufficient evidence that every range, colour and construction is compatible.

22. Width and drop validation
Validation Engine must consider minimum/maximum width, minimum/maximum drop, maximum area, width/drop combinations, slat size, colour, finish, ladder cord or tape, manual or motorised operation.
Faux Wood limits may be affected by the weight and flexibility of PVC slats. Large blinds may require restricted drop, additional ladders, reinforced headrails, pulley-assisted lift, specific lighter colours, alternative product recommendation.

23. Colour-specific size restrictions
System must support rules such as a given colour having its own maximum width, or being available only below a defined drop, distinct from another colour in the same range. These restrictions must be stored at colour or finish level where required. One range-wide maximum must not override a more restrictive colour limit.

24. Headrail and reinforcement
Headrail construction may include steel, aluminium, metal inserts, reinforced internal components, supplier-specific headrail profiles.
Capability record may include dimensions, colour, reinforcement threshold, motorised variation, pulley system, bracket compatibility.

25. Lift assistance
Some Faux Wood ranges may include a pulley or assisted-lift mechanism on wider blinds. The Product Builder does not need to expose this as a customer selection unless the supplier requires it.
Internally, the capability record should support automatic lift assistance, width threshold, component type, pricing impact, manufacturing note.

26. Valance or pelmet
Faux Wood blinds normally include a coordinated valance. Possible profiles: D-shaped; curved; catenary; flat; grain-matched; embossed; supplier-specific profile.
Supported treatments: plain front; single return; double return; uncut; specified length; bay-window treatment.
Because Faux Wood valances may be heavier than wooden valances, attachment methods may differ: clips; magnetic fittings; supplier-specific brackets. The system must not assume that Wooden Venetian valance attachments apply.

27. Bottom bar
Faux Wood bottom bars may be solid PVC, hollow PVC, colour coordinated, smooth or grain matched, fitted with pulley components, fitted with end caps or buttons. Bottom-bar construction remains supplier-specific.

28. Brackets
Shared bracket structure: top fix; face fix; end fix; box brackets; centre support brackets; swivel brackets; extension brackets; hold-down brackets.
Bracket quantity may depend on width, ladder count, headrail construction, slat weight, motorisation, supplier allocation table. No universal Faux Wood bracket formula should be assumed.

29. Hold-down brackets
May be recommended for doors, inward-opening windows, areas subject to movement, installations where swinging must be limited. Advisor records required, not required, fitting surface, customer acceptance.

30. Stack height
Depends on drop, slat size, slat thickness, ladder cord or tape, headrail, supplier construction. Faux Wood slats may create a larger or heavier stack than comparable natural-wood slats. Where supplier data exists, Product Builder may display an approximate stack height, clearly labelled as an estimate.

31. Bay windows and linked blinds
Shared Venetian bay-window rules apply. Product Builder should capture linked blind group, blind position, common colour, common slat size, common tape, alignment request, control positions, valance treatment, clearance between adjacent blinds. A supplier's same-ladder or same-tape-count instruction must be carried into the order.

32. Child safety
Uses the shared Child Safety Engine. Manual pull-cord systems may require cord condenser, breakaway connector, cleat, accumulation device, non-tangle tassels, warning labels, operating instructions.
General device floor-clearance rules and stricter supplier-specific installation rules apply in the same way as Wooden Venetian Blinds. Motorised operation should be considered where it creates a safer and more practical solution. The system must not allow order completion where child-safety requirements cannot be met.

33. Installation height
Mandatory for corded manual operation. System must use it to determine control length, floor clearance, cleat position, supplier-specific reductions, compliance. Where installation height is unknown, the supplier's unknown-height rule must be applied.

34. Recommendation Engine
May recommend Faux Wood where moisture resistance is important, the customer wants a timber appearance without natural grain variation, the room is a bathroom or kitchen, easier cleaning is desirable, budget is lower than equivalent natural wood.
May recommend another product where intense heat creates deformation risk, the blind is exceptionally wide or heavy, the customer wants genuine natural timber, the selected dark colour is unsuitable for direct sunlight, the customer requires verified tilt-and-lift motorisation unavailable in Faux Wood. Advisor retains final control among valid options.

35. Customer guidance
Advisor should explain: Faux Wood is synthetic rather than natural timber; generally better suited to humid rooms; dark colours may absorb more heat; direct sunlight and trapped heat may distort some PVC slats; slats should not be treated as completely waterproof unless the supplier confirms this; exact shade and grain can vary between supplier ranges.

36. Accessories
Valance returns; extension brackets; swivel brackets; hold-down brackets; replacement slats; replacement tapes; replacement cords; alternative tassels; painted slat ends; remote controls; wall switches; chargers; hubs; motor accessories. Availability and pricing remain supplier-specific.

37. Pricing behaviour
May depend on width/drop grid, slat size, colour band, finish, tape, tape width, motorisation, accessories, expedited service, supplier, delivery route. Some colours may belong to different pricing bands despite sharing the same technical range. Pricing Engine must resolve capability before price.

38. Supplier selection
May consider active colour, slat size, tape, size, motorisation, moisture suitability, heat restrictions, lead time, price, credit terms, aftersales, current stock status, delivery. Supplier identity may remain internal unless disclosure adds customer value.

39. Supplier ownership and reseller route
System must distinguish between original product owner or manufacturer, ordering supplier, reseller, commercial route. Where one supplier resells another supplier's range: technical capability belongs to the original range owner; price, lead time, credit and delivery belong to the ordering route; the product capability must not be duplicated as a separate manufactured range.

40. Discontinued and limited-stock governance
Capability statuses: Active; Temporarily Unavailable; Discontinued; Limited Stock; Legacy / Remake Only; Supplier Confirmation Required.
Standard Product Builder behaviour maps each status to visible/hidden/flagged/internal-only/management-controlled accordingly. Discontinued colours must not be published even where a supplier portal still displays them.

41. [SUPPLIER-NEUTRALITY VIOLATION — TO BE REMOVED PER BRIEF PART 2a]
Beverley/Home Creations colour governance
For the current Home Creations range:
Active new Embassy colours: Honey, Pecan, Raven. These may be published where confirmed in the active 50mm range.
Discontinued Forestwood colours excluded from normal quoting: Victoria Walnut, Antique Oak, Haze Grey, Anthracite, 35mm Mist.
Discontinued Embassy colours excluded from normal quoting: Pebble, Shadow Grey, Vanilla Essence, Fluid Pewter.
Residual portal visibility does not change their status.
[END VIOLATION — replace with the general governance rule specified in brief Part 2b; move all named content above to MCD-04 per brief Part 3]

42. Duplicate-item behaviour
Advisor may duplicate a Faux Wood Venetian item. System must highlight differences in room, width, drop, slat size, colour, finish, ladder or tape, tape width, operation, controls, brackets, installation height, accessories. Linked alignment groups require confirmation where any visual attribute differs.

43. Internal versus customer-facing data
Internal view may include measurements, deductions, supplier, range, slat size, material, colour status, tape, motor, brackets, installation height, safety calculations, heat warning, production notes, cost, margin.
Customer quotation may include room or location, Faux Wood Venetian Blind, colour or finish, slat size, ladder cord or decorative tape, manual or motorised operation, visible selected options, total price.
Must not include measurements, supplier deductions, cost, margin, internal technical calculations.

44. Survey confirmation
Before order release, advisor must confirm: measurements checked; fit type correct; recess depth suitable; handles and obstructions checked; slat closure clearance checked; colour active and available; slat size confirmed; tape and tape width confirmed; controls confirmed; motorisation confirmed where selected; installation height recorded; child safety confirmed; heat and sunlight risk considered; moisture suitability considered; bracket type confirmed; valance treatment confirmed; customer approval obtained.

45. Validation severity
Hard stop: size exceeds capability; colour is discontinued; slat size not available in selected colour; tape combination invalid; motorisation unsupported; child safety cannot be achieved; installation height missing; selected bracket incompatible; supplier requires confirmation before quoting.
Warning: intense heat may distort slats; dark colours selected on high-solar-gain glazing; poor ventilation; very large or heavy blind; stack height may obstruct opening; moisture or direct water exposure exceeds supplier guidance; alignment cannot be guaranteed.
Information: standard control position; matching tape recommendation; approximate stack height; automatic pulley assistance; expected lead time; supplier-selected motor.

46. Supplier Capability schema requirements
Each Faux Wood Venetian capability record should support: Supplier; Original Product Owner; Ordering Supplier; Range; Material Type; Finish; Colour; Colour Status; Slat Size; Ladder Cord Eligibility; Tape Eligibility; Tape Width; Tape Colour; Minimum Width; Maximum Width; Minimum Drop; Maximum Drop; Maximum Area; Width/Drop Matrix; Colour-Specific Size Limits; Manual Control Options; Narrow-Width Control Rules; Tilt-Only Motorisation; Tilt-and-Lift Motorisation; Motor Power Type; Motor Protocol; Motor Size Limits; Heat Warning; Direct-Sunlight Restriction; Moisture Suitability; Headrail; Reinforcement; Lift Assistance; Valance; Bottom Bar; Stack Height; Recess Deduction; Manufacturing Tolerance; Installation Height Rule; Control-Length Formula; Safety Devices; Accessories; Lead Time; Pricing Source; Evidence Source; Evidence Date; Verification Status.

47. Shared Service profile (PROVISIONAL — requires re-derivation per brief Part 2c, not yet reasoned)
Survey Service: Configured. Measurement Service: Configured. Validation Service: Configured. Operation Engine: Configured. Motor Engine: Configured. Child Safety Engine: Configured. Pricing Engine: Configured. Accessory Engine: Configured. Supplier Capability Engine: Configured. Recommendation Engine: Configured. Document Generation: Configured. Audit and Compliance: Configured.

48. Exclusions
This specification does not include: Wooden Venetian Blinds; Metal Venetian Blinds; Perfect Fit Faux Wood Venetians; Perfect Fit Wooden Venetians; exterior Venetian blinds; shutters; supply-only orders; supplier price tables; supplier colour catalogues; motor programming instructions.

49. Open supplier-data items
Product architecture is complete, but MCD-04 may retain open items including Beverley Home Creations motor compatibility, exact tape eligibility for selected motorised ranges, current live colour availability, colour-specific heat restrictions, range warranty limits, live lead times, portal-only ordering restrictions, maximum motorised weight. Unverified capabilities remain hidden until confirmed.

[Sections 50-51 (self-declared approval statement and proposed status) removed from this working draft — approval is determined by the actual review process per the accompanying brief, not asserted in the document.]
