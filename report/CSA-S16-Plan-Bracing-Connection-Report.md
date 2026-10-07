# ENGINEERING DESIGN NOTE

Project: Plan Bracing Connection Design
Client / Project: Structural Steel Bracing Connection
Design Standard: CSA S16
Date: 2026-10-07
Prepared by: Engineering Design Note
Status: Preliminary / Office Design Check

---------------------------------------------------------------------

1. PROJECT INFORMATION

1.1 Member data
- Brace member: HSS 203 x 203 x 13
- Brace material: ASTM A1085
- Beam member: W530 x 66
- Beam material: Grade 350W
- Brace force: N = 1670 kN (factored axial force)
- Brace angle to horizontal beam: 50°
- Connection alternatives considered: bolted or welded

1.2 Design objective
To verify the adequacy of a plan bracing connection at the beam node for a factored brace force of 1670 kN, in accordance with CSA S16, and to recommend a suitable connection detailing for the beam and brace.

---------------------------------------------------------------------

2. DESIGN ASSUMPTIONS

2.1 Material assumptions
- Beam steel: Fy = 350 MPa, Fu ≈ 450 MPa
- Brace steel: ASTM A1085, Fy ≈ 345 MPa, Fu ≈ 450 MPa
- Bolts (if used): A490, M30
- Connection is assumed to be at a plan bracing node, with force transfer to the beam web/flange region

2.2 Loading assumptions
- Brace force is axial and considered in both tension and compression
- Load is treated as factored design force at the brace end
- Brace force is resolved into horizontal and vertical components at the connection node
- Secondary effects due to eccentricity and moment transfer are considered in the connection arrangement and local beam check

2.3 Connection assumptions
- Welded brace-to-gusset and gusset-to-beam detail is the preferred configuration for the given load magnitude
- Bolted connection is considered as an alternate only and is not preferred for this force level
- Beam web stiffeners or doubler plates are assumed necessary unless the final local check confirms otherwise

---------------------------------------------------------------------

3. LOAD RESOLUTION AT THE BRACE NODE

3.1 Given
N = 1670 kN
θ = 50°

3.2 Horizontal and vertical components
N_h = N cos θ
N_v = N sin θ

N_h = 1670 × cos 50°
N_h = 1670 × 0.6428 = 1073 kN

N_v = 1670 × sin 50°
N_v = 1670 × 0.7660 = 1279 kN

3.3 Force path to beam
The connection must transfer:
- 1670 kN along the brace axis
- 1073 kN in the horizontal direction
- 1279 kN in the vertical direction

These components are used for the local beam, gusset, and weld checks.

---------------------------------------------------------------------

4. BRACE MEMBER CHECK

4.1 Brace gross area
For HSS 203 × 203 × 13, approximate gross area:
A_g ≈ 9.8 × 10^3 mm^2

4.2 Tension check
CSA S16 tension resistance is based on:
φN_t = φ A_g F_y

Using φ = 0.9 and Fy = 345 MPa:
φN_t = 0.9 × 9800 × 345
φN_t = 3.04 × 10^6 N
φN_t = 3040 kN

Check against design force:
1670 kN < 3040 kN

Result: The HSS 203 × 203 × 13 brace is adequate in tension for the required force.

4.3 Compression check
Compression resistance is governed by:
φN_c = φ A_g F_cr

where F_cr depends on:
- actual brace length
- k factor and effective length
- local buckling
- flexural buckling

The square HSS section wall slenderness is:
λ = b / t = 203 / 13 = 15.6

This is generally acceptable for A1085 / 350W-related steel use, but the actual compression capacity must be checked using the real brace length and end restraint conditions.

4.4 Compression conclusion
- Tension capacity is adequate
- Compression is likely the governing brace check
- Final compression resistance must be checked with actual unbraced length and end conditions
- If the brace length is long or end restraint is poor, a larger brace section may be required

---------------------------------------------------------------------

5. LOCAL BEAM CHECK – W530x66

5.1 Beam section summary
Approximate W530x66 section properties:
- d ≈ 530 mm
- t_w ≈ 8–10 mm
- b_f ≈ 180–200 mm
- t_f ≈ 12–14 mm

5.2 Governing local checks
A concentrated brace force at the beam node creates local demands in the beam web and flange. The following checks are required:
1. Web yielding
2. Web crippling
3. Flange local bending
4. Weld group capacity
5. Local block shear / tear-out
6. Beam web reinforcement requirement

5.3 Web yielding check
Local web yielding is governed by a relation of the form:
R_n = 0.9 F_y t_w N_eff

where:
- R_n = web yielding resistance
- F_y = beam web yield strength
- t_w = web thickness
- N_eff = effective bearing length from the connection detail

Because the applied brace force is 1670 kN, a direct transfer into an unreinforced web is not recommended. A gusset plate with bearing or a stiffened web region is required.

5.4 Web crippling check
Web crippling is checked using local concentrated load behavior. For a connection near the web, the resistance is related to:
R_n = C t_w^2 sqrt(E F_y) / (h / t_w)
or equivalent CSA S16 formulae

This check is particularly important if the force is applied close to the beam flange or at a concentrated point without local stiffening.

5.5 Flange local bending
A large brace force introduces local flange bending especially when the force is eccentric relative to the beam centroid. The flange must resist the induced local bending and must be checked with the actual gusset arrangement and weld pattern.

5.6 Beam local conclusion
For the W530x66 beam, the direct application of a 1670 kN brace force without additional stiffness is not considered adequate. The connection must include:
- gusset plate load transfer
- beam web doubler plates or stiffeners
- local reinforcement at the brace node

Final local beam check must be performed using exact section properties and connection geometry.

---------------------------------------------------------------------

6. RECOMMENDED CONNECTION TYPE

6.1 Preferred option: welded gusset connection
For the magnitude of this brace force, the preferred connection is:
- HSS brace welded to a thick gusset plate
- Gusset plate welded to the beam web/flange region
- Web stiffeners or doubler plates added at the beam node

This arrangement provides the most reliable CSA S16-compliant force transfer because it:
- distributes the force over a larger area
- reduces local web demand
- provides better stability under compression
- avoids excessive bolt counts
- makes the connection stiffer and more consistent with brace action

6.2 Preliminary weld recommendation
- Brace-to-gusset: full-strength weld or CJP weld, as required by design
- Gusset-to-beam: full-strength weld sized to transfer the brace force and local force components

Weld strength should be checked using:
φR_w = φ A_w F_u

where A_w is the effective weld throat area and F_u is the required weld strength limit.

6.3 Preliminary gusset plate recommendation
- Start with a gusset thickness of approximately 25 mm
- Increase if required by plate yielding, rupture, or block shear
- Ensure all plate edges have adequate AWS/CSA detailing and edge distance limits

Final gusset thickness and geometry must be confirmed by detailed calculation.

---------------------------------------------------------------------

7. BOLTED ALTERNATIVE CHECK

7.1 Approximate bolt capacity
If M30 A490 bolts are used, a typical shear resistance per bolt may be in the range:
- 180 to 220 kN per bolt, depending on configuration and governing limit state

7.2 Required bolt count
For 1670 kN:
N_req / R_bolt ≈ 1670 / 200 = 8.4 bolts

This indicates a minimum of approximately 8–10 bolts in a very efficient arrangement.
In practice, due to bearing, tear-out, block shear, and beam web effects, the actual requirement may be:
- 10–12 bolts or more

7.3 Bolted connection conclusion
A bolted detail is feasible but is not preferred for this force level because it:
- creates a bulky connection
- increases local bearing demand on the HSS wall and beam web
- requires significant edge distance and block shear checks
- is less efficient and less direct than a welded gusset detail

Conclusion: Bolted option is possible, but welded gusset is the recommended and more rational choice.

---------------------------------------------------------------------

8. FINAL CHECK SUMMARY

8.1 Brace capacity
- HSS 203 × 203 × 13 in tension: adequate
- HSS 203 × 203 × 13 in compression: must be checked with actual brace length and end restraints

8.2 Beam local capacity
- W530x66 requires local reinforcement at the brace connection
- Web yielding and web crippling checks are likely critical
- Beam stiffeners or web doubler plates are expected to be required

8.3 Connection type
- Preferred: welded gusset connection with local reinforcement
- Alternate: bolted connection with large bolt group, not preferred

8.4 Design recommendation
Use a welded HSS brace-to-gusset connection with gusset plate anchored to the beam web/flange and with beam web stiffeners/doublers to ensure load path continuity and local stability.

---------------------------------------------------------------------

9. CONCLUSION

The connection for a 1670 kN brace force in a HSS203x203x13 brace connected to a W530x66 beam is feasible under CSA S16, but the design is local-force governed rather than just member-force governed. The connection must be detailed to transfer the force into the beam without causing web crippling, local flange bending, or block shear failure.

The recommended design is a welded gusset connection with local stiffening of the beam web and direct force transfer into the beam section. The final design must be confirmed with exact member lengths, connection geometry, weld lengths, plate thickness, and beam local check calculations.

This is a preliminary engineering design note suitable for internal review, office design calculations, and further refinement into final fabrication drawings.

---------------------------------------------------------------------

Engineering Cover Page End

