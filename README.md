# Mathematical Crystallography
## Description
Classification of Spacial Distribution of Molecules.
## Homogenous Z-space.
In Nature, molecules are often spaced uniformly. We will call such an arrangement a Crystal. Due to this uniformity we can predict the location of additional molecules should the crystal grow.
We will refer to all locations (occupied or ones that could be) as Molecules.
In mathematical parlance a Crystal is therefore a homogenous Z<sup>n</sup> subspace of the Euclidean Space E<sup>n</sup>.
Here, n = 3 for Spacial distribution but what we discuss will often apply to linear (n = 1) and planar (n = 2) cases.
If we select molecule O as the origin and if {e<sub>1</sub>,...,e<sub>n</sub>} is a basis of Z<sup>n</sup> then Molecules of the Crystal can be parametrized by

> { O + m<sub>1</sub>e<sub>1</sub> + ...  + m<sub>n</sub>e<sub>n</sub> } where m<sub>n</sub> are integers

The arrangement is then determined by metric properties (e<sub>i</sub>|e<sub>j</sub>) of the simplex spanned by the basis - tetrahedron (n = 3), triangle (n = 2), segment (n = 1).
It is possible however for 2 bases with different metric properties to represent the same arrangement.
One way the classification can be achieved is by finding a way to produce a unique 'special' basis (simplex).
Two arrangements would then be deemed identical if the corresponding simplices were metrically equivalent.

![Z_basis](img/Z_basis.jpg "Title")

## Selection of Canonical Basis
The following works in planar case (will deal with spacial case later)
* Select a Molecule closest to O and another at the same distance or at the next closest distance (excluding the opposite of the first selected)
* When choosing between multiple possible molecules for the 2nd selection, choose the one closest to the opposite of the 1st selection.
![Z_special](img/Z_special.jpg "Title")

## Mirror Symmetries and Root System
A Euclidean plane is called Plane of Symmetry if it cuts the Crystal into 2 pieces which are mirror images of each other.
If such plane contins O and the line through O, perpendicular to it contains molecules then the vector from O to the first such molecule is called a Root.
The set of all Roots is called the Root System. It turns out that if a Root System is present then it is made of all molecules closest to the origin
and (possibly) all those which are next-closest. In the latter case we will have 2 types of Roots: the 'short' and the 'long' ones.
In order to refer to a Root System in an unambigouos way we again need a rule to find a 'special' basis. The rule for the planar case is

* select any root
* select 2nd root to be one closest to the opposite of the 1st one.

## Dynkin Graph
The metric properties of a simplex is given by 5 numbers (3 angles + 2 ratios) in spacial case and  2 numbers ( 1 angle and 1 ratio) planar case.
In Dynkin approach these numbers are derived from a graph-like shape.
It is used in very special cases where angles are 90&deg;, 120&deg;, 135&deg;, 150&deg; and the lenght ratio is determined by the angle.
Each vertex of the graph represents a root and the stroke of the edge segment which joins 2 vertices represents the angle between the corresponding roots (absence of edge indicates the right-angle).
The strokes are determined by the following table.
<table>
  <caption>
    Relation between Angle and Length Ratio
  </caption>
  <thead>
    <tr>
      <th scope="col">Angle(deg)</th>
      <th scope="col">Ratio</th>
      <th scope="col">Line Width</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th scope="row">90&deg;</th>
      <td>not defined</td>
      <td>no line drawn</td>
    </tr>    
    <tr>
      <th scope="row">120&deg;</th>
      <td>1:1</td>
      <td>single stroke</td>
    </tr>
    <tr>
      <th scope="row">135&deg;</th>
      <td>1:&radic;2</td>
      <td>double stroke</td>
    </tr>
    <tr>
      <th scope="row">150&deg;</th>
      <td>1:&radic;3</td>
      <td>tripple stroke</td>
    </tr>
  </tbody>
</table>

Once such graph is produces, the only additional information that may be needed is: 'Which end of the graph edge represents the long root ?'
That last piece of information is produced by drawing a less-then sign '>' in the middle of the edge where (just like in case of numeric inequality) the oppening is towards the longer root).

## Irreducible Root Systems
Each connected component of a Dynkin graph is itself a Dynkin. If the Dynkin Graph is connected then the corresponding Root System is called Irreducible. Each Irreduciple Dynkin is assigned a letter
(A - G) with a subscipt indicating the dimension (3 for Space, 2 for Plane, 1 for line). The Root Systems named A-D can have any subscript (appear in all dimensions).
The Root Systems named (E-G) can only appear in certain dimensions. They are called 'Exceptional'.
This naming may result in an overlaps in lower dipensions and in such cases we name using alphabetically first letter. In particular, the only root system on a line is named A<sub>1</sub>.
A non irreducible root system is named by listing the names of its irreducible components separated by an (x) symbol.
## Chambers and Alcoves
The partitions of Space produced by planes of symmetry through O are called Chambers. Chambers are infinite, cone-like shapes. The rule to select the 'special' basis of the Root System can now be stated as

* Select the roots perpendicular to the 3 faces of the Chamber.

A Chamber always contains a Root (and a short one in case of a long/short Root System). The Simplex obrained by cutting the Chamber with a plane that orthogonally bisects that (short) root is called an Alcove.
All planes which extend alcove faces are planes of symmetries and flipping the alcove repeatedly around its faces will tile the entire Space without gaps.
