**************************
Tesseract Geometry Package
**************************

Background
==========
This package contains geometry types used by Tesseract including primitive shapes, mesh, convex
hull mesh, octomap and signed distance field.

Features
========

#. Primitive Shapes

   * Box
   * Cone
   * Capsule
   * Cylinder
   * Plane
   * Sphere

#. Mesh
#. Convex Mesh
#. SDF Mesh
#. Octree

Creating Geometry Shapes
========================

   .. rli:: https://raw.githubusercontent.com/steviedale/tesseract/update/tesseract_documentation/tesseract_geometry/examples/create_geometries_example.cpp


Example Explanation
-------------------

#. Create a box.

   .. rli:: https://raw.githubusercontent.com/steviedale/tesseract/update/tesseract_documentation/tesseract_geometry/examples/create_geometries_example.cpp
      :language: c++
      :start-after: // Shape Box
      :end-before: // Shape Cone

#. Create a cone.

   .. rli:: https://raw.githubusercontent.com/steviedale/tesseract/update/tesseract_documentation/tesseract_geometry/examples/create_geometries_example.cpp
      :language: c++
      :start-after: // Shape Cone
      :end-before: // Shape Capsule

#. Create a capsule.

   .. rli:: https://raw.githubusercontent.com/steviedale/tesseract/update/tesseract_documentation/tesseract_geometry/examples/create_geometries_example.cpp
      :language: c++
      :start-after: // Shape Capsule
      :end-before: // Shape Cylinder

#. Create a cylinder.

   .. rli:: https://raw.githubusercontent.com/steviedale/tesseract/update/tesseract_documentation/tesseract_geometry/examples/create_geometries_example.cpp
      :language: c++
      :start-after: // Shape Cylinder
      :end-before: // Shape Plane

#. Create a plane.

   .. rli:: https://raw.githubusercontent.com/steviedale/tesseract/update/tesseract_documentation/tesseract_geometry/examples/create_geometries_example.cpp
      :language: c++
      :start-after: // Shape Plane
      :end-before: // Shape Sphere

#. Create a sphere.

   .. rli:: https://raw.githubusercontent.com/steviedale/tesseract/update/tesseract_documentation/tesseract_geometry/examples/create_geometries_example.cpp
      :language: c++
      :start-after: // Shape Sphere
      :end-before: // Manually create mesh

#. Create a mesh.

   .. rli:: https://raw.githubusercontent.com/steviedale/tesseract/update/tesseract_documentation/tesseract_geometry/examples/create_geometries_example.cpp
      :language: c++
      :start-after: // Manually create mesh
      :end-before: // Manually create signed distance field mesh

   .. Note::

      This shows how to create a mesh provided vertices and faces. You may also use utilities in tesseract_scene_graph mesh parser to load meshes from file.

#. Create a signed distance field mesh.

   .. Note::

      This should be the same as a mesh, but when interpreted as the collision object it will be encoded as a signed distance field.

   .. rli:: https://raw.githubusercontent.com/steviedale/tesseract/update/tesseract_documentation/tesseract_geometry/examples/create_geometries_example.cpp
      :language: c++
      :start-after: // Manually create signed distance field mesh
      :end-before: // Manually create convex mesh

   .. Note::

      This shows how to create a SDF mesh provided vertices and faces. You may also use utilities in tesseract_scene_graph mesh parser to load meshes from file.

#. Create a convex mesh.

   .. Warning::

      This expects the data to already represent a convex mesh. If yours does not load as a mesh and then use tesseract utility to convert to a convex mesh.

   .. rli:: https://raw.githubusercontent.com/steviedale/tesseract/update/tesseract_documentation/tesseract_geometry/examples/create_geometries_example.cpp
      :language: c++
      :start-after: // Manually create convex mesh
      :end-before: // Create an octree

   .. Note::

      This shows how to create a convex mesh provided vertices and faces. You may also use utilities in tesseract_scene_graph mesh parser to load meshes from file.

#. Create an octree.

   .. rli:: https://raw.githubusercontent.com/steviedale/tesseract/update/tesseract_documentation/tesseract_geometry/examples/create_geometries_example.cpp
      :language: c++
      :start-after: // Create an octree
      :end-before: }

   .. Note::

      It is beneficial to prune the octree prior to creating the tesseract octree shape to simplify

   Octree support multiple shape types to represent a cell in the octree.

   * BOX **tesseract_geometry::Octree::SubType::BOX**
   * SPHERE_INSIDE **tesseract_geometry::Octree::SubType::SPHERE_INSIDE**
   * SPHERE_OUTSIDE **tesseract_geometry::Octree::SubType::SPHERE_OUTSIDE**
