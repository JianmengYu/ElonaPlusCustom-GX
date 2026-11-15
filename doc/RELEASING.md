# Releasing new versions

These are the steps taken when releasing a new version of Custom-GX.

1. Update `README.md` with the latest version number. Mirror the latest Elona+ release somewhere and update the download link in `README.md` to point to it. (Ano deletes old versions of Elona+ with each new release.)
2. Edit `CHANGELOG.md` and record the important changes.
3. Update the version numbers in `main.hsp` where needed. Commit the changes and push.
4. Tag the release with Git and push the new tag.
```
git tag -a 2.05.1.1 -m 2.05.1.1
git push origin 2.05.1.1
```
5. Build a new .exe with `hsed3.exe` as detailed in `README.md`. Use [Resource Hacker](https://www.angusj.com/resourcehacker/) or [Resource Cracker](https://www.pelock.com/products/resource-cracker) to replace its icon with `2.05-custom-gx/icon.ico`.
6. Download the latest CGX release archive from [here](https://github.com/Ruin0x11/ElonaPlusCustom-GX/releases). Rename the archive with the new version number.
7. Copy
- `elonapluscgx.exe`, `README.md`, `CHANGELOG.md`,
- `ADDT.dll` and `GuruGuruSMF4.hpi` from `2.05-custom-gx/`,
- `config.txt` from `dist/2.05-custom-gx/original`, and everything in `dist/2.05-custom-gx`
to the downloaded release archive.
8. Make a new release using GitHub under the newly pushed tag.
9. Download the new release and test it under a fresh install of Elona+ to make sure everything works.
