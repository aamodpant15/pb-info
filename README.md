# pb-info

### What is it?
This is the repository for the published Github page of family_tree info, written in React.js
(Working a more humble python version, that implements the same functions in the terminal, for those who do not want to deal with GUI's)


A generalized React.js version will be uploaded soon, which will have access to the source files.

Features included will be:

1. Login authorization(information will not be public)
1. Searching for members by Name, and Address
2. Getting relatives (mother, father, children, spouse)
3. Getting ancestry (Fraternal Generations)
4. Getting siblings
5. Getting immediate family
6. More features as time goes on

### How does it work?

Excel Sheet is read and converted to a JSON file. (This JSON file is a nice thing to have, and can be used for personal projects as well)
JSON file is read, and `Member` data structures are created for each entry. Each `Member` has attributes as each column of the excel sheet.
`Member` is wrapped by a `Node` data structure. This has a `data` attribute which is a pointer to its respective the `Member` class.
`Node` has other attributes like `mother`, `father`, and `spouse`, which are references to `Member` objects, and `children` which is an array of references to `Member` objects.

A "Tree" is then created by adding references to each `Node`'s attributes.
This tree may be a disconnected tree, as there might be people who do not have entries, which leaves empty spots in a family tree.
