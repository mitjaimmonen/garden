# Bitti notes

repositories should support both local storage and firestore.
For FDroid version, firebase code should not exist at all.

For each data source, two implementations (firestore, localstorage)

Repositories have combined logic using both data source implementations, but compile time constants should remove firebase code from Fdroid flavor.

