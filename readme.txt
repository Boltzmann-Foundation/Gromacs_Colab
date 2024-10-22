
split -b 49M gromacs-2024.3_prebuilt.tar gromacs_part_prebuilt_

%%shell
# Define base URL and file prefixes
base_url="https://raw.githubusercontent.com/Boltzmann-Foundation/Gromacs_Colab/main/"
file_prefix="gromacs_part_prebuilt_"

# List of parts to download
parts=("aa" "ab" "ac" "ad" "ae" "af" "ag" "ah")

# Loop to download each part
for part in "${parts[@]}"; do
  wget -q "${base_url}${file_prefix}${part}" 
done

cat gromacs_part_* > gromacs-2024.3_prebuilt.tar


