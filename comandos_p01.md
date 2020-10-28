# Comandos de la Práctica 01
## Nombre(s) Apellido(s)

# Parte I. 

**Respuesta 1:**

echo $0
/bin/bash 

**Respuesta 2:**

mkdir data filtered raw_data meta scripts figures archive


**Respuesta 3:**

mv ./filtered ./data
mv ./raw_data ./data

**Respuesta 4:**

Se organiza para que las investigaciones se puedan reproducir, compartir y reutilizar.

# Parte II.

**Respuesta 1**

ls -l
chmod +x delay.sh

**Respuesta 2**

sh delay.sh

**Respuesta 3**

sleep 30

**Respuesta 4**

sh delay.sh &
kill $!

##Parte III

**Respuesta 1**

SarsCov-2.txt

**Respuesta 2**

mv sequence.fasta sarscov2_genome.fasta
mv sequence.gff3 sarscov2_genome.gff3

mv sequence.fasta splike_c.fasta
mv sequence(1).fasta splike_b.fasta
mv sequence(2).fasta splike_a.fasta


##Parte 4

**Respuesta 1**

ln -s ./data/raw_data/splike_c.faa ./data/filtered/
ln -s ./data/raw_data/splike_b.faa ./data/filtered/
ln -s ./data/raw_data/splike_a.faa ./data/filtered/

**Respuesta 2**

cat> ./data/filtered/glycoproteins.faa

**Respuesta 3**

head -n 1 splike_a.faa splike_b.faa splike_c.faa 

pdb|6VXX|A Chain A, SARS-CoV-2 spike glycoprotein

pdb|6VXX|B Chain B, SARS-CoV-2 spike glycoprotein

pdb|6VXX|C Chain C, SARS-CoV-2 spike glycoprotein


**Respuesta 4**

cat ./data/raw_data/splike_a.faa ./data/raw_data/splike_b.faa ./data/raw_data/splike_c.faa > ./data/filtered/glycoproteins.faa

**Respuesta 5**

mv ./data/raw_data/splike_* ./archive/

Ya no sirven la ligas

**Respuesta 6**

head -n 3 sarscov2_genome.fasta
zless sarscov2_assembly.fasta.gz | head -n 3 sarscov2_assembly.fasta

**Respuesta 7**

awk '/^>/' sarscov2_genome.fasta | wc -l
zless sarscov2_assembly.fasta.gz | awk '/^>/' | wc -l

**Respuesta 8**

zless SRR10971381_R2.fastq.gz | awk '/@/' | wc -l

**Respuesta 9**

.fasta y .faa son iguales corresponden a nucleótidos
.fastqc corresponde a aminoácidos

**Respuesta 10**

-S mantiene la tabla horizontal

**Respuesta 11**

head -n 5 sarscov2_genome.gff3 | less -S





















