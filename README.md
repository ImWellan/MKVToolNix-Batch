[README Wellan.md](https://github.com/user-attachments/files/31284200/README.Wellan.md)
# MKVToolNix by Wellan

An unofficial modified build of MKVToolNix focused on faster batch remuxing workflows.

This build keeps the normal MKVToolNix tools and adds a custom Batch workflow inside the GUI. It is meant for users who work with seasons, folders or groups of Matroska files that usually share the same track structure.

## What the Batch tab does

The Batch tab helps you prepare many MKV files at once instead of editing each file manually in the standard multiplexer.

Main features:

- Add source folders or source files and analyze them as a batch.
- Use one file as the global model for the batch.
- Compare other files against the model and mark them as ready, different or excluded.
- Quickly keep or remove tracks across many files.
- Edit track language, track name, default-track flag and forced-display flag.
- Ignore attachments and chapters when comparing file differences.
- Optionally ignore video track titles when detecting differences.
- Queue remux jobs from the Batch interface.
- Replace source files only after a successful remux, so the original file is not overwritten if the job fails.
- Rename files in batch with enumeration, character removal and string movement tools.
- Prepare synchronization values for tracks, such as delay in milliseconds.

## Basic workflow

1. Open the Batch tab.
2. Add a source folder or source files.
3. Wait for the files to be analyzed.
4. Review the global model and the selected file tracks.
5. Exclude files or tracks that should not be remuxed.
6. Adjust track language, names, default flags or forced flags if needed.
7. Choose the destination behavior in the Batch preferences.
8. Launch the batch.

If a file has no actual change to apply, the batch workflow can skip remuxing it instead of creating a pointless duplicate.

## Batch renaming

The Renaming tab is used to preview and apply file-name changes before remuxing. Renamed files stay in the batch list so you can still review and remux them afterward.

Available renaming methods include:

- Enumeration
- Character removal
- String movement

Each method can be enabled independently. The preview column shows the resulting file name before applying the rename operation.

## Language

This portable package is configured to start in English by default. The interface language can still be changed from the MKVToolNix GUI preferences.

## File layout

The package is organized to keep the main folder easier to read:

- `mkvtoolnix-gui.exe`, `mkvmerge.exe`, `mkvinfo.exe`, `mkvextract.exe` and `mkvpropedit.exe` are launchers.
- The real executables use the `.real.exe` suffix.
- Shared `.dll` files are stored in the `DLL` folder.
- The launchers automatically add the `DLL` folder to the runtime search path before starting the real MKVToolNix executable.

Use `mkvtoolnix-gui.exe` to start the application normally.

## Important notes

- This is an unofficial modified build, not the official MKVToolNix release.
- MKV files are remuxed, not re-encoded. Video/audio quality should not be changed by remuxing alone.
- Always test the workflow on a small set of files before processing an entire library.
- Keep backups of important media files, especially when using source-file replacement.

## Original MKVToolNix documentation

Original MKVToolNix documentation and notices are included in the `doc` folder.

The official MKVToolNix website is:

https://mkvtoolnix.download/
