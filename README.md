# Dataset artefact

The dataset is uploaded to this repository as three 7zip archive slices.

The dataset is an archive folder and every folder under it contains a `.jar` file that contains the corresponding bytecode of a Java project (usually downloaded from Maven repository), a smt folder that contains `.smt2` SMT-LIB scripts, and a `simple_statistics.json` file that contains statistics.

The statistics are collected with Python scripts, and every entry corresponds to a `.smt2` script. Solvers are tested on the script and their performances are recorded in the statistics.

The SMT-LIB scripts and the statistics are referred to as "the full dataset", as opposed to "the thin dataset" whose entries are selected with the Python statement `item["undefined_function_count"] < 1 and len(item["api_count"]) > 0` from the `simple_statistics.json` file.
