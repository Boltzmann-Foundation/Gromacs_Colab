
%%shell
wget -q "https://github.com/Boltzmann-Foundation/Gromacs_Colab/blob/main/gromacs_part_aa"
wget -q "https://github.com/Boltzmann-Foundation/Gromacs_Colab/blob/main/gromacs_part_ab"
wget -q "https://github.com/Boltzmann-Foundation/Gromacs_Colab/blob/main/gromacs_part_ac"
cat gromacs_part_* > gromacs-2024.3_prebuilt.tar

split -b 90M gromacs-2024.3_prebuilt.tar gromacs_part_

cat gromacs_part_* > gromacs-2024.3_prebuilt.tar
