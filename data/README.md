# Publication catalog exports

The publication catalog is snapshotted from the institutional publication
database by the nightly warehouse export job. Snapshots are cut into fixed
windows of 160 records; the window boundaries are inclusive on both ends.

The final window is a verification re-export triggered by the nightly QA job.
Because the export cursor is inclusive at the boundary, the verification
snapshot starts 50 records before the end of the previous window.

File naming: `catalog_rows_<first>-<last>[_verification].csv`.
