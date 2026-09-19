# Five-Finger Tendon-Driven Simulation

**Development snapshot:** September 19, 2026  
**Stage:** Simulation and control prototype  
**Tools:** MuJoCo 3.3.7 · Python · CAD mesh processing

## Objective

Explore tendon routing and control across a full hand before committing to further hardware iterations. The model uses the current full-hand CAD geometry and supports three control interfaces: direct tendon force, target joint angle, and commanded tendon shortening in millimeters.

## Model and implementation

| Element | Current implementation |
| --- | --- |
| Geometry | 141 CAD components imported from the full-hand STL |
| Joints | 15 degrees of freedom: 14 flexion/extension joints and little-finger MCP lateral motion |
| Actuation | 30 main tendons: 28 for flexion/extension and 2 for lateral motion |
| Tendon branches | 14 Y branches; each branch pair shares one main actuator |
| Displacement control | Unilateral force through a virtual series-elastic model, with gradual length commands |
| User interface | Separate finger tabs, force and angle modes, relaxation, return-to-reference, and reset controls |

The thumb currently has MCP and IP flexion/extension. Its metacarpal is fixed; CMC opposition is not represented. Branch guides, wrist anchors, and virtual wrapping cylinders support the simulation and still require a corresponding manufacturable routing design.

## Recorded checks

The development reports record 22 angle-target cases and 32 tendon-displacement cases, plus integration checks for combined commands, reset, input limits, and return-to-reference behavior.

Selected small-angle configurations, including individual 20-degree flexion tests and sampled lateral-motion cases, did not show tendon-centerline intersections with CAD surfaces. These are discrete checks of idealized centerlines, not continuous-path or finite-rope clearance guarantees.

At simultaneous 45-degree flexion, intersections remain for the thumb, middle finger, and ring finger. At 90 degrees, all fingers show intersections. Small-angle debugging is the appropriate starting point.

## Current limitations

- Mesh contact is disabled. Controller tracking does not establish collision-free physical motion.
- Ligament-shaped and cross-joint parts are bound as rigid geometry rather than modeled as deformable structures.
- Mass, inertia, damping, return springs, joint axes, and actuator limits have not been calibrated against hardware.
- Rope friction, rope-to-rope contact, and spool-motor dynamics are not modeled.

## Next experiments

Resolve large-angle routing, calibrate joint motion against the physical prototype, and establish finite-diameter rope clearance before interpreting the model as a manufacturing or performance prediction.

[Back to the bionic hand](README.md) · [Portfolio home](../../README.md)
