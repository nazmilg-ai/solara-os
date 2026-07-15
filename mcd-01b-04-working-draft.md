MCD-01B-04 — Wooden Venetian Blinds
Status: Working Draft — Unverified (downgraded from self-declared "Approved Draft Baseline"; has not been through branch/review/Decision Register/verification process)
Version: v1.0 (pre-review)
Parent Document: MCD-01A — Sales MVP Product Engine Architecture
Product Family: Standard Blinds
Reference Role: Venetian-family reference implementation (proposed)

1. Purpose
This document defines the supplier-neutral product specification for Wooden Venetian Blinds within Solara OS.
It establishes: the shared product structure; advisor-facing configuration fields; survey and validation requirements; manual and motorised operation models; child-safety behaviour; recommendation logic; accessory handling; document-generation rules; supplier-capability dependencies.
Supplier-specific ranges, dimensions, colours, motor compatibility, control lengths, pricing and manufacturing restrictions remain within MCD-04 — Product Library & Supplier Management.
This specification must not encode one supplier's technical rules as universal Wooden Venetian behaviour.

2. Product definition
A Wooden Venetian Blind is a made-to-measure internal blind comprising: a headrail; horizontal wooden slats; ladder cord or decorative ladder tape; a matching or coordinated bottom bar; a valance or pelmet; manual or supported motorised controls; installation brackets; applicable child-safety devices.
The product provides adjustable privacy and light control through slat tilting and may be fully raised where the selected construction supports lift operation.

3. Product-family position
Standard Blinds -> Wooden Venetian Blinds
Wooden Venetian Blinds remain separate from: Faux Wood Venetian Blinds; Metal Venetian Blinds; Perfect Fit Wooden Venetian Blinds; Perfect Fit Metal Venetian Blinds; shutters.
Perfect Fit is a separate construction-system family and must not appear as a sub-configuration within this standard product.

4. Relationship to the Venetian reference implementation
Wooden Venetian Blinds are proposed as the reference implementation for the Venetian family.
The following concepts are expected to be reused by Faux Wood and Metal Venetian specifications where applicable: slat size; tilt and lift behaviour; ladder cord or tape; control-side arrangement; bracket allocation; valance or pelmet treatment; stack height; hold-down brackets; slat alignment; child-safety validation; motorisation eligibility; width/drop capability checks.
Later Venetian specifications must reference this shared structure and document only genuine product differences.

5. Design principles
Advisor-first. Supplier-neutral. Capability-driven. Non-assumptive. Advisory rather than restrictive.

6. Product material structure
The shared product supports natural-wood material categories including: real wood; Basswood; Bamboo; Abachi; other supplier-supported natural timber types.
Material subtype is technically significant because it may affect: maximum width; maximum drop; slat thickness; blind weight; bottom-bar profile; valance profile; finish availability; motorisation; stacking height; natural variation guidance.
Supplier Capability must therefore resolve below range level where required: Supplier -> Range -> Material Subtype -> Construction Capability

7. Core advisor workflow
Room; Window reference; Fit type; Width; Drop; Material or range presentation; Slat size; Colour; Ladder cord or tape; Tape width and colour, where applicable; Manual or motorised operation; Control arrangement; Valance or pelmet; Bracket and extension requirements; Hold-down brackets; Installation height; Child-safety validation; Supplier capability resolution; Price calculation; Internal survey confirmation.

8. Measurement mode
8.1 Wooden Venetian Blinds support Recess and Exact. The selected mode must be stored explicitly.
8.2 Recess: advisor enters measured recess width and drop; supplier-specific deductions applied automatically; customer-facing quotation must not display measured width, measured drop, supplier deductions, manufacturing size.
8.3 Exact: advisor enters required finished blind size; system must not apply a recess deduction.
8.4 Measurement validation (Survey Engine): width; drop; installation height; recess depth; handle projection; sill projection; obstructions; window opening direction; fitting surface; bracket position; multiple-blind alignment; bay-window relationships.

9. Recess suitability and clearance
Wooden Venetian Blinds require sufficient recess depth for the selected slat size, headrail, bracket, valance, control mechanism.
Known survey behaviour: a shallow recess combined with a projecting handle may make a Wooden Venetian unsuitable; a face-fixed Roller Blind with reverse roll may be a better option. This is recommendation logic, not a universal prohibition.

10. Slat size
Common supplier-supported sizes include 35mm and 50mm. Other sizes may be introduced through Supplier Capability without changing this product specification. The system must only display slat sizes supported by the selected supplier, range, material subtype, colour, construction, operating method. A colour may be available in one slat size but not another.

11. Colour and finish
Possible finish categories: painted; stained; grain finish; soft grain; gloss; natural finish; two-tone or coordinated options where supported.
Colour record must support: active; discontinued; temporarily unavailable; limited stock; remake or legacy only; supplier confirmation required.
Discontinued colours must not appear in the normal advisor-facing Product Builder, even where they remain visible in a supplier portal for residual stock or remakes.
Natural timber variation must be acknowledged: grain variation; shade variation; colour absorption differences; knots or natural markings; possible minor warping or movement. This is an expected material characteristic rather than automatically a manufacturing defect.

12. Ladder construction
Supports ladder cord and decorative ladder tape. Availability resolved by range, material subtype, slat size, colour, operation type, motorisation, width/drop limits.
12.1 Ladder cord: colour may be matched to slat, coordinated, supplier default, advisor-selectable where supported.
12.2 Decorative tape: tape width; tape colour; default matching tape; alternative coordinated tape; contrast tape; weave type; surcharge. Known tape widths include 10mm, 19mm, 25mm, 38mm as illustrative examples — this list is not exhaustive and is not a claim that all widths are available on all ranges. The system must not assume that all tape widths work with all slat sizes.
12.3 Matching tape: advisor may select supplier-recommended matching tape or alternative supported tape. Where the same tape count or alignment is required across multiple blinds, the order must carry a special instruction.

13. Slat alignment
May be requested for adjacent windows, bay windows, multiple blinds in the same opening, visually related blinds. System must capture: alignment required Y/N; linked item references; same number of ladders/tapes required Y/N; special instructions. Subject to supplier capability and manufacturing tolerance; must not be guaranteed merely because two blinds have the same drop.

14. Manual operation
Shared system must support: split controls; both controls left; both controls right; reverse split controls; supplier-standard arrangement; forced standard arrangement; no controls for very narrow blinds. Actual availability filtered by Supplier Capability.
14.1 Narrow blinds: some supplier ranges impose no controls below a defined width, standard controls only within a narrow-width band, restricted same-side controls. The Product Builder must apply the exact range rule rather than one universal width threshold.
14.2 Advisor-facing controls: where more than one arrangement is valid, the advisor may select it. Where the supplier forces a configuration, the system should apply it automatically and explain the reason.

15. Motorisation
Motorisation is an optional configuration and not an assumed family-wide capability. The shared Operation Engine supports: Manual; Motorised — Tilt Only; Motorised — Tilt and Lift.
15.1 Tilt Only: adjusts slat angle, does not raise/lower.
15.2 Tilt and Lift: adjusts slats and raises/lowers; available only on supported supplier ranges and constructions.
15.3 Capability resolution: Supplier + Range + Material Subtype + Slat Size + Ladder Cord or Tape + Width + Drop + Area or Weight + Required Function + Power Type + Motor System.
15.4 Power and control types: battery powered; rechargeable; mains powered; hardwired; radio remote; wall switch; hub compatibility; smart-home compatibility.
15.5 Motor selection behaviour: advisor-selectable; system-recommended; supplier-selected; factory-confirmed. Where exact motor sizing requires finished weight or supplier engineering, the system should record the required operation and pass final selection to the supplier.
15.6 Unconfirmed motorisation: Motorisation Availability: Not Confirmed / Advisor Visibility: Hidden / Quoting Status: Disabled. The system must not infer availability from a similar range.

16. Motorised construction restrictions
Product Builder must support restrictions such as: tilt-and-lift only with ladder cord; taped blinds limited to tilt-only; motorisation limited to 50mm slats; motorisation limited by colour or finish; minimum motorised width; width/drop combination tables; mains-only tilt-and-lift; battery-only tilt operation; standard brackets required; swivel brackets incompatible with motorisation. These are Supplier Capability values, not shared Wooden Venetian rules.

17. Width, drop, area and weight validation
Validation Engine must evaluate: minimum/maximum width; minimum/maximum drop; maximum area; width/drop combination limits; finished weight; ladder or tape construction; motorised versus manual; material subtype; colour or finish restrictions. A simple maximum-width field is insufficient. Capability may need to be expressed as a conditional (if width <= X then max drop Y; if width > X then max drop Z) or a full eligibility matrix.

18. Headrail
Headrail properties remain supplier-specific: width; height; depth; material; colour; reinforcement; steel or aluminium inserts; motorised headrail variation. Customer-facing interface does not need to expose headrail dimensions unless relevant to suitability.

19. Valance or pelmet
Possible profiles: contour; chamfered; flat; angled; cambered; catenary; supplier-specific decorative profile.
Product Builder must support: plain front; single return; double return; uncut; specified length; bay-window treatment; shared or continuous appearance; magnetic, clip or dual-lock attachment where relevant.
19.1 Recess and Exact behaviour: supplier may determine a different valance length for Recess orders, Exact orders, return configurations — remains in Supplier Capability.
19.2 Customer-facing terminology may use "Valance / Pelmet."

20. Bottom bar
May vary by material subtype, slat size, colour, supplier range. Possible profiles: trapezoid; rectangular; T-shaped; supplier-specific moulded profile. Capability record must support profile, material, dimensions, colour, end caps or buttons, pulley assistance where applicable.

21. Brackets
Shared product supports: top fix; face fix; end fix; box brackets; centre support brackets; swivel brackets; extension brackets; spring brackets where supported.
21.1 Bracket quantity may depend on width, ladder count, supplier table, headrail reinforcement, motorisation — there is no universal Wooden Venetian bracket formula.
21.2 Extension brackets: survey must capture whether additional projection is required for handles, tiles, architraves, window vents, structural obstructions. Extension length and compatibility remain supplier-specific.
21.3 Motorised restrictions: some motorised constructions require standard brackets and do not permit swivel brackets. The system must enforce the exact range rule.

22. Hold-down brackets and side guides
May be recommended for doors, inward-opening windows, frequently moving panels, locations where the blind may swing. Advisor records required Y/N, fitting surface, customer acceptance. Side guides or guide wires may be supported on selected supplier ranges, treated as capability-driven accessories.

23. Stack height
Depends on drop, slat size, slat thickness, material subtype, ladder cord or tape, supplier construction. Product Builder may display an estimated stack height where supplier data exists, labelled as approximate.

24. Bay windows and multiple blinds
Bay-window configurations require separate blind items unless a supplier-specific combined solution exists. System should support linked blind group; left/centre/right references; common slat size; coordinated colour; common tape selection; alignment request; valance treatment; bracket conflicts; control-side coordination; clearance between blinds. Individual headrails are the normal assumption. Any curved or specialist system must be treated as a separate supplier capability, not assumed within the standard product.

25. Child safety
Mandatory, handled through the shared Child Safety Engine.
25.1 Safe-by-Design priority: advisor should consider inherently safe options first, including motorised operation, genuinely cordless supported systems, concealed or tensioned controls.
25.2 Pull-cord systems: shared engine must account for cord condenser or consolidator, breakaway behaviour, accumulation device, cleat, non-tangle tassels, cord stops, warning labels, operating instructions. BBSA guidance states accumulation devices should be securely fitted at least 1.5m from the floor and as near to the headrail as possible; pull-cord blinds must not be installed below the applicable safety height.
25.3 Breakaway threshold: where a breakaway device is used, the applicable minimum floor-clearance threshold may be 0.6m rather than 1.5m.
25.4 Supplier-specific rules: shared engine must distinguish between general safety-device floor clearance, minimum blind installation height, supplier control-length formula, range-specific minimum, breakaway minimum floor clearance. Supplier-specific stricter rules take precedence over the general minimum.
25.5 Installation obligations: installer must fit required safety devices securely, leave warning labels attached, leave product instructions with the customer, show the customer how the blind and safety device operate.
25.6 Refusal or unsafe installation: blind must not be completed where mandatory child-safety requirements cannot be met. Any refusal or customer objection must follow the platform Child Safety Refusal workflow.

26. Installation height
Required field for corded manual Wooden Venetian Blinds. System must use it to determine maximum permitted control length, cleat position, floor clearance, supplier-specific control reduction, whether the selected configuration is compliant. Where installation height is unknown, the supplier's unknown-height rule must be applied. The system must never invent or approximate a control length.

27. Natural-material guidance
Advisor should explain real wood is a natural product: grain differences; shade differences; small tonal changes between slats; minor bowing; knots or natural markings; colour change over time; reaction to heat or moisture.
27.1 Moisture: Wooden Venetian Blinds generally not the preferred recommendation for bathrooms, wet rooms, rooms with persistent high humidity, locations exposed to condensation. A Faux Wood Venetian may provide better long-term performance. Recommendation logic rather than an absolute prohibition unless the supplier specifically restricts the product.
27.2 Heat and direct sunlight: advisor should consider intense direct sunlight, conservatory-like heat, glazing that creates heat build-up, large south-facing windows. Supplier guidance and warranty limitations must be available to the advisor.

28. Recommendation Engine
May surface guidance on privacy, bathrooms/high moisture (recommend Faux Wood), shallow recesses (warn), bedrooms (not total-blackout), street-facing windows (recommend Venetian over Roller), large/heavy blinds (recommend motorisation where supported and commercially sensible). Advisor retains final control.

29. Accessories
Additional valance; valance returns; extension brackets; swivel brackets; hold-down brackets; guide wires; alternative tassels; painted or stained slat ends; spare slats; replacement tapes; replacement cords; remote controls; wall switches; chargers; hubs; motor accessories. Availability and pricing remain supplier-specific.

30. Pricing behaviour
May depend on width/drop price grid, square-metre pricing, slat size, material subtype, finish, ladder cord or tape, tape type, motorisation, control system, accessories, expedited lead time, supplier, delivery route. Pricing Engine must resolve the cheapest valid supplier only after capability validation. Price must not override technical suitability.

31. Supplier selection
May consider technical capability, product colour, slat size, tape availability, motorisation, size, lead time, price, credit terms, aftersales, remake process, delivery, current stock status. Advisor may see Good/Better/Best recommendations, but supplier identity may remain internal unless there is a reason to disclose it.

32. Discontinued and limited-stock items
Supplier portal visibility does not equal normal availability. Capability status must support: Active; Temporarily Unavailable; Discontinued; Limited Stock; Legacy / Remake Only; Supplier Confirmation Required. Standard Product Builder behaviour maps each status to visible/hidden/flagged/internal-only/management-controlled accordingly. A discontinued colour must not be presented to a customer merely because a supplier portal still allows selection.

33. Duplicate-item behaviour
Advisor may duplicate a Wooden Venetian item for another window. System must clearly highlight differences in room, window reference, width, drop, colour, slat size, ladder/tape, operation, controls, brackets, installation height, accessories. Any deviation from a linked alignment group must trigger confirmation.

34. Internal versus customer-facing data
Internal view may include measurements, deductions, supplier, range, material subtype, motor, controls, brackets, installation height, child-safety calculations, production notes, price breakdown, cost, margin.
Customer quotation must include room or location, Wooden Venetian Blind, colour or finish, slat size where useful, ladder cord or decorative tape, manual or motorised operation, relevant visible options, total price.
Customer documents must not display measurements, deductions, supplier trade terminology, cost price, internal margin, technical motor calculations.

35. Survey confirmation
Before order release, advisor must confirm: measurements checked; fit type correct; recess depth suitable; handles and obstructions checked; slat closure clearance checked; colour confirmed; natural-wood variation explained; tape and tape width confirmed; controls confirmed; motorisation confirmed where selected; installation height recorded; child-safety method confirmed; bracket type confirmed; valance treatment confirmed; alignment instructions recorded; customer approval obtained.

36. Validation severity
Hard stop: size exceeds confirmed capability; motorisation unsupported; selected slat/tape combination invalid; child safety cannot be achieved; supplier colour discontinued; required installation data missing; selected bracket incompatible with motorisation.
Warning: moisture may make Faux Wood more suitable; shallow recess or handles may obstruct operation; natural variation requires customer explanation; stack height may reduce clear glass; large blind may be heavy to operate manually; alignment requested but cannot be guaranteed.
Information: default control arrangement; supplier-selected motor; approximate stack height; standard tape recommendation; expected lead time.

37. Supplier Capability schema requirements
Each Wooden Venetian capability record should support: Supplier; Original Product Owner; Ordering Supplier; Range; Material Subtype; Finish; Colour; Colour Status; Slat Size; Ladder Cord Eligibility; Tape Eligibility; Tape Width; Tape Colour; Minimum Width; Maximum Width; Minimum Drop; Maximum Drop; Maximum Area; Width/Drop Matrix; Manual Control Options; Narrow-Width Control Rules; Tilt-Only Motorisation; Tilt-and-Lift Motorisation; Motor Power Type; Motor Protocol; Motor Size Limits; Bracket Compatibility; Headrail; Valance; Bottom Bar; Stack Height; Recess Deduction; Manufacturing Tolerance; Installation Height Rule; Control-Length Formula; Safety Devices; Accessories; Lead Time; Pricing Source; Evidence Source; Evidence Date; Verification Status.

38. Shared Service profile (PROVISIONAL — requires re-derivation per brief Part 1c, not yet reasoned)
Survey Service: Configured. Measurement Service: Configured. Validation Service: Configured. Operation Engine: Configured. Motor Engine: Configured. Child Safety Engine: Configured. Pricing Engine: Configured. Accessory Engine: Configured. Supplier Capability Engine: Configured. Recommendation Engine: Configured. Document Generation: Configured. Audit and Compliance: Configured.

39. Exclusions
This specification does not include: Faux Wood Venetian Blinds; Metal Venetian Blinds; Perfect Fit Wooden Venetians; Perfect Fit Metal Venetians; exterior Venetian blinds; shutters; supply-only orders; customer self-measurement workflow; detailed supplier price tables; supplier colour lists; supplier-specific motor programming instructions.

40. Open data items
Product architecture is complete, but MCD-04 may retain supplier-level open items such as: unconfirmed motor compatibility; current colour availability; portal-only restrictions; final motor weight limits; current lead times; supplier-specific warranty terms; discontinued stock status; live pricing updates. An open supplier data item must not prevent eventual approval of this supplier-neutral product specification. It must, however, keep the affected capability hidden until verified.

[Sections 41-42 (self-declared approval statement and proposed status) removed from this working draft — approval is determined by the actual review process per the accompanying brief, not asserted in the document.]
