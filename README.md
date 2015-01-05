ThreeDeify
==========

An idea for creating a stereo image from a 2D source

1. Analyze blobs to find potential objects in the source image.
2. Analyze optic flow in recent video frames.
3. For each blob and for the background, average contained optic flow vectors.
4. Generate two left/right displacement map images with blob areas (and background) displaced by opposite amounts with magnitude equal to the averaged optic flow on the area.
5. Use the displacement maps to render the stereogram.

The idea is that parallax on closer objects should produce more optic flow over recent frames. Then the objects as identified by the blob analyzer can be shifted by a displacement map to affect a stereo image.

Alternately - use blob detection on a denser optic flow field. Or, use the optic flow blob analysis *together* somehow to find objects instead of just moving blob detected areas by optic flow amounts.
