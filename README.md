# scoop-strike
Instructions for installing Strike on Windows using Scoop.

## Steps for each new Strike build
1. Compress the files and folders created by the Xojo build process into a `.zip` file and rename to `strike-XXX-win64.zip` (where `XXX` is the version number). The version number must be bigger than the current one for Scoop to correctly update Strike
2. Draft a new release for Strike and upload the Windows and macOS files. Copy the URL for the Windows download
3. Update the `version` key to the new version number
4. Set the URL in `strike.json` to the Windows zip URL
5. Determine the Windows zip file's SHA256 value with the Terminal command: `openssl sha256 [file]`
6. Replace the SHA56 value in the JSON file `hash` key with the new one
7. Commit and push the changes in the JSON file to GitHub.
