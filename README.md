# Spatial transcriptomics/10x visium data preparation
This repository aims to detail the processing of space ranger pipeline from FATSTQ files to gene expression matrix.

## Spaceranger
### T6 - Download spaceranger
`curl -o spaceranger-3.0.1.tar.gz "https://cf.10xgenomics.com/releases/spatial-exp/spaceranger-3.0.1.tar.gz?Expires=1724480948&Key-Pair-Id=APKAI7S6A5RYOXBWRPDA&Signature=HVB5cU5s~le6QS8S9EQ2SUvHVcA9gfjTMzY70dyQpK2PTP14pvlwIke2T8lWbtnyuRJRegeameYZ~C80p6NNl3mH7VF1dQh6SY6HeBOfqcXbtaIOErNaPeqzfStiRJvtHIGDTNHgMbuO5qT6VBZgEqoCNQkuLSx3VS~i2kNoBd0BT5HXdKaeHS4BzcdiPtP2fNusG0esOzNY16WnASLkx4RB-U3KeouHOd8T8Ry9RlTwdNAJev2m3ZGoCmW2HiXoenQJ9tafmhAwkd9vltkETXSXfXf1FVi0kKvi84yOrmzebngTylJeuX7L~o6bGIOx1Mb~pkElN0trwcJx7jCqNA__"`

### T6 - Install spaceranger
- Unpack, `tar -xzvf spaceranger-3.0.1.tar.gz`

- Prepend the Space Ranger directory to your $PATH. This allows you to invoke the spaceranger command.
`$ export PATH=/home/xpan7/spaceranger-3.0.1:$PATH`

or add it to `.bashrc` where you can find `nano ~/.bashrc`
After editing, save the changes and exit the editor by pressing Ctrl + X, then Y, and finally Enter.

- To apply the changes made in .bash_profile without restarting the terminal, you can run:
`source ~/.bashrc`

- To test if spaceranger is installed successfully

navigate to your own dir, `/rsrch5/home/trans_mol_path/xpan7/project`, to ensure the output of testing sample is stored in your own dir instead of yuanlab dir.

then `spaceranger testrun --id=tiny`


### Seadragon - spacerager
There is spaceranger module installed in Seadragon, please refer to `sample_specific_spaceranger_hpc.lsf` to run spaceranger in Seadragon.

Note that,

- You'll see the following after `module load spaceranger`, but it doesn't mean the spaceranger version is 1.1.0; it's actually 3.0.1 if using `spaceranger --version` to check
`Reference data are located in path
                /rsrch3/scratch/reflib/REFLIB_data/spaceranger-1.1.0`

- The error logs can be found in .out files. If you cannot find the error info in .err files, also check with .out files.


## Data
