# Preliminary Design Report
# Plan Bracing Connection Design
# CSA S16, HSS203x203x13 Brace to W530x66 Beam

Prepared for office design note use.

## 1. Project information
- Brace member: HSS 203 x 203 x 13, ASTM A1085
- Beam member: W530 x 66, Grade 350W
- Brace force: N = 1670 kN (factored axial force)
- Brace orientation: 50° to horizontal beam
- Connection alternatives considered: bolted or welded
- Structural standard: CSA S16-24 (or current edition adopted by project)

## 2. Design assumptions
- Steel grade for beam and plate: 350W, Fy = 350 MPa, Fu ≈ 450 MPa
- Brace steel: ASTM A1085, Fy ≈ 345 MPa, Fu ≈ 450 MPa
- Load is considered as design axial force in both tension and compression
- Brace force is treated as a factored member force at the brace node
- Connection is assumed to be a plan bracing connection at a beam node
- Local checks for the beam are based on the concentrated force transferred from the brace to the beam web/flange region

## 3. Brace force components at the connection
The brace force is resolved into the beam axes:

N_x = N cos(50°)
N_y = N sin(50°)

N_x = 1670 x cos(50°)
N_x = 1670 x 0.6428 = 1073 kN

N_y = 1670 x sin(50°)
N_y = 1670 x 0.7660 = 1279 kN

Therefore, the connection must transfer:
- 1670 kN along the brace axis
- 1073 kN horizontal component
- 1279 kN vertical component

These components are to be considered in the connection force path and local beam check.

## 4. Brace member resistance check
### 4.1 Gross area of HSS203x203x13
For a square HSS 203 x 203 x 13, the approximate gross area is:
A_g ≈ 9.8 x 10^3 mm^2

### 4.2 Tension resistance
CSA S16 tension check:
φN_t = φ A_g F_y

Using φ = 0.9 and Fy = 345 MPa:
φN_t = 0.9 x 9800 x 345
φN_t = 3.04 x 10^6 N
φN_t = 3040 kN

Compare with design force:
1670 kN < 3040 kN

Result: Brace tension capacity is adequate.

### 4.3 Compression resistance
Compression resistance must be checked for global flexural buckling and local buckling.
The governing equation is:
φN_c = φ A_g F_cr

where F_cr depends on:
- actual unbraced length of brace
- brace end restraint and rotation
- steel grade
- section classification

For HSS203x203x13, the local wall slenderness is:
λ = b/t = 203/13 = 15.6

This is generally acceptable for the section class for A1085 / 350W-type steel, provided the member is not excessively slender by the actual fabrication and detailing standards.

However, compression is usually governing for a brace at this force level. The final check must be performed with the exact brace length and effective length factor K, because:
- if K L is long, the member may be compression-governed
- if the brace is short and well restrained, the compression member can be acceptable

Therefore, the preliminary conclusion is:
- tension capacity is sufficient
- compression must be verified with actual brace length
- a larger brace may be required if the panel is long or end restraint is poor

## 5. Beam local check – W530x66
The beam local check is critical because the brace force is not simply a member force; it is transferred into the beam web/flange region and causes concentrated-force effects.

### 5.1 Beam section overview
For a W530x66 beam (typical values), approximate section properties are:
- d ≈ 530 mm
- t_w ≈ 8–10 mm
- b_f ≈ 180–200 mm
- t_f ≈ 12–14 mm

Use exact values from the section file for final verification.

### 5.2 Force transfer into beam
The brace force introduces concentrated effects into the beam due to the axial brace force and eccentricity. The connection must be designed so that the force path is direct and stable.
The critical local checks are:
- web yielding under concentrated load
- web crippling
- flange local bending
- local yielding near weld group
- block shear and tear-out around welds/bolts

### 5.3 Web yielding check
Web yielding is checked using a local bearing width and the effective length of bearing. For concentrated load at a brace node, the governing concept is:
R_n = 0.9 F_y t_w N_eff

where:
- R_n = web yielding resistance
- F_y = yield strength of beam web
- t_w = beam web thickness
- N_eff = effective bearing length from the connection detail

The force from the brace is 1670 kN, which is very high for a concentrated load on a W530x66 web unless the force path is distributed using a gusset, stiffeners, or doubler plates.

Therefore, a direct welded or bolted force transfer into a thin web without additional stiffening is not recommended.

### 5.4 Web crippling check
Web crippling is checked by the local concentrated force at the connection zone. A typical form for design is:
R_n = 0.75 t_w^2 sqrt(E F_y) / (h / t_w)
(or equivalent CSA S16 expression for concentrated loads)

This relation shows that the beam web can be vulnerable to crippling when a large brace force is introduced close to a flange or near an unreinforced web panel.

Result: For the W530x66, web stiffeners or doubler plates are expected to be required when the brace force is 1670 kN.

### 5.5 Flange local bending
The brace force may induce local bending in the beam flange where a gusset or weld group is attached. The flange is checked for local bending and plate action using the tributary width and the applied force components.

Because the brace force has both vertical and horizontal components, the connection must be arranged to minimize eccentricity and avoid significant moment on the beam flange.

## 6. Connection concept recommendation
### 6.1 Preferred design: welded gusset connection
For a brace force of 1670 kN, the more robust approach under CSA S16 is a welded gusset connection.

Recommended arrangement:
- Brace end welded to a gusset plate
- Gusset welded to the beam web/flange region
- Beam web doubler plates and/or stiffeners provided at the connection zone
- Gusset plate designed to transfer the brace force into beam web/flange without causing local failure

This arrangement is preferred because:
- it distributes the brace force more effectively
- it avoids excessive bolt group size
- it reduces local tearing at the beam web
- it is better suited to a large axial brace force in both tension and compression

### 6.2 Weld design
Recommended welds:
- Brace-to-gusset: full-strength weld, full circumference if HSS is used
- Gusset-to-beam: full-strength weld, sized for the load path to the beam web/flange

A practical starting point is:
- brace-to-gusset: complete joint penetration or equivalent full-strength weld
- gusset-to-beam: fillet or CJP weld designed to the resist shear and eccentricity forces

Final weld size must be checked using:
φR_w = φ A_w F_u
for weld throat area and electrode strength.

### 6.3 Gusset plate sizing
The gusset plate must resist:
- axial force component along brace axis
- shear transfer to beam framing
- local bending caused by eccentricity
- block shear at the weld path

Preliminary thickness selection:
- start with 25 mm gusset plate for a large brace node
- increase thickness if required by local bending or shear checks

The final plate thickness must be confirmed using:
- gusset plate yielding and rupture checks
- block shear around welded connection
- effective width of plate under axial load

## 7. Bolted alternative check
### 7.1 Feasibility of M30 A490 bolts
If a bolted connection is required, the connection will require a significant bolt group.

Approximate shear capacity per M30 A490 bolt depends on the governing check and connection condition, but a practical range is around:
- 180 to 220 kN per bolt in shear, depending on hole type and connection configuration

For 1670 kN:
N_required / R_one_bolt ≈ 1670 / 200 = 8.4 bolts

This suggests a minimum of roughly 8–10 bolts in a highly favorable arrangement. In practice, because of:
- bearing on HSS wall and gusset plate
- tear-out and edge distances
- block shear
- eccentricity
- beam web compression

the actual required number of bolts will likely be 10–12, or more.

### 7.2 Bolted connection concerns
A bolted solution may be feasible but is generally less efficient and more cumbersome for a 1670 kN brace force. Major concerns include:
- bolt bearing on HSS wall
- tear-out at gusset edges
- block shear in the connecting plates
- local yielding of beam web near bolt group
- connection stiffness and eccentricity effects

Conclusion: bolted is possible, but welded gusset is the preferred and more practical solution for this load level.

## 8. Final recommended detail
The final practical connection is:
- HSS brace welded to thick gusset plate
- Gusset plate welded to beam web/flange with stiffeners
- Beam web doubler plates and stiffeners at the connection zone
- Connection layout symmetric around the brace axis to minimize eccentricity
- Additional local reinforcement if the load is applied near the web toe or near the flange edge

This is the most rational CSA S16 detailing approach for a 1670 kN brace connection.

## 9. Design summary
- Brace HSS203x203x13: adequate in tension
- Brace compression: requires actual length check
- Beam W530x66: local beam checks are critical and will likely require stiffener/doubler plates
- Preferred connection: welded gusset connection
- Bolted M30 A490 may be possible but is not preferred for this magnitude of force
- Final design must include local beam web/flange checks, gusset plate checks, weld checks, and brace compression buckling verification

## 10. Conclusion
For the given conditions, a robust CSA S16-compliant plan bracing connection can be developed, but the detailed design should be based on a welded gusset arrangement with beam web reinforcement. The connection cannot be finalized without checking the exact brace length, beam connection geometry, and local stiffener arrangement.

This report is a preliminary office note for design development and should be used as the basis for the final calculation package and final node detailing.

---

Sketch note:
The connection detail should be developed as a welded HSS brace-to-gusset connection with a gusset plate attached to the beam web/flange and reinforced with stiffeners/doublers. The brace force acts at 50° to the beam and is resolved into horizontal and vertical components.

This report is suitable for copy/paste into Word, and the accompanying SVG sketch can be imported into Word as a figure.




