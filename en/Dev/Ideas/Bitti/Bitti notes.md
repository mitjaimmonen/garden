---
Planted: 2025-01-14
Tended: 2025-02-16
---
# Bitti notes

*Planted: `= this.Planted`*
*Tended: `= this.Tended`*

---


repositories should support both local storage and firestore.
For FDroid version, firebase code should not exist at all.

For each data source, two implementations (firestore, localstorage)

Repositories have combined logic using both data source implementations, but compile time constants should remove firebase code from Fdroid flavor.

---
#### Backups

**Firebase Firestore:**
- The easiest solution
- Dangerous as data can be misused 
	- needs cloud functions to stop costs
	- Possibly needs to be hosted by an ltd company to mitigate risk
- Multiple sign in options
- Secure and safe

**Self hosted:**
- A lot more difficult setup
- Security must be foolproof - difficult, ltd again might be needed to mitigate risk

**Supabase:**
- Open source alternative to firebase
- Cost control - no risk of unplanned costs

---
#### Icon picker

- Support SVG images instead of font-icons
- Colors:
	- Two colors with tint (basic icons)
	- Full colors, no tint (emojis)
- Importing own svg files?
- Backup support -> make sure data usage does not shoot up