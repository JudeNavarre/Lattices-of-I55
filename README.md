# Lattices-of-I55
This repository contains the text file I55lattices.txt, a list of the sets of relators for all the torsion-free vertex-regular cocompact lattices of Bourdon's building I_{5,5} which is formatted for use with GAP 4. 

Each entry in the list in I55lattices.txt is itself a list containing 5 lists of length 5 with entries consisting of digits between 0 and 9. Each digit i represents a generator or inverse generator for the corresponding torsion-free vertex-regular cocompact lattice of I_{5,5} according to the following rule: i represents the generator x_i for i < 5, and i represents the inverse generator x_{i-5}^{-1} for i >= 5. Each 5-digit list represents a relator. For example, the list \[ 0, 0, 1, 0, 2 \] represents the relator x_0\*x_0\*x_1\*x_0\*x_2. 

In addition, the repository contains the text file relatorstogroups.txt, which contains a GAP 4 program which will convert the sets of relators in I55lattices.txt into finitely presented groups. 

## Getting Started
Download the files I55lattices.txt and relatorstogroups.txt and copy them to your GAP directory. You should now be able to read both files using the GAP commands
```
Read("I55lattices.txt");
```
and
```
Read("relatorstogroups.txt");
```
The sets of relators in I55lattices will now be defined in GAP as the list named 'I55lattices.' 

The following command will then take the list 'I55lattices' and return the corresponding list of finitely presented groups.
```
RelatorsToGroups(I55lattices);
```
The function RelatorsToGroups can also be applied to any sublist of I55lattices.

## Authors

* **Samantha Smith** 

## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details
