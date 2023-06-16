

# Mergetable: The dataframe merge runner for CRISPResso2 out data.
[![pyversions](https://img.shields.io/badge/python-3-blue)]()

**Mergetable** is the dataframe merge runner for CRISPResso2 out data. It designed to enable rapid and intuitive interpretation of genome editing experiments.

## Install

#### Requirements

The script has been tested using the following softwares and their versions:

- python=3.10.11
- numpy=1.24.3
- pandas =2.0.2

If the dependency package is missing, the most convenient way is to install it directly with the command pip.

```python
$ pip install numpy pandas
```

Clone the repository, install the dependencies and start the application. You must copy the [Mergetable](https://github.com/ligeng-k/Mergetable) directory together.

```shell
git clone git@github.com:ligeng-k/Mergetable.git

cp -r Mergetable.linux.x86_64 you_installation_path/
```

#### By example (Mergetable.linux.x86_64):

```shell
$ Mergetable/Mergetable.linux.x86_64
├── Mergetable
└── Mergetable.pyarmor.rkey

1 directory, 2 files
```

Verify that Mergetable is installed using the command:

```shell
# Mergetable.linux.x86_64
$ export PATH=$PATH:you_installation_path/Mergetable.linux.x86_64
$ Mergetable -h
Mergetable -i <inputfile> -n <filename> -o <outputfile>
```

#### By example (Mergetable.windows.x86_64):

```shell
$ Mergetable/Mergetable.windows.x86_64
├── Mergetable.py
└── pyarmor_runtime_000000
    ├── __init__.py
    ├── __pycache__
    │   └── __init__.cpython-310.pyc
    └── pyarmor_runtime.pyd

3 directories, 4 files
```

Verify that Mergetable is installed using the command:

```shell
# Mergetable.linux.x86_64
$ python C:\Users\DZ\Desktop\Mergetable\Mergetable.py -h
Mergetable.py -i <inputfile> -n <filename> -o <outputfile>
```

### Parameter List

-h : show a help message and exit.

-i : Sample list file.

-n : The name of the form you need to merge.

-o : Output folder to use for the analysis.




## Getting Started

#### Run test

```python
$ pip install numpy pandas
```

```python
# samplelist.txt
$ cat test/samplelist.txt
1,2,3
```

Quantification_window_nucleotide_percentage_table.txt

|      | C          | C          | T          | C          | A          |
| ---- | ---------- | ---------- | ---------- | ---------- | ---------- |
| A    | 0          | 0.00110742 | 0          | 0.00110742 | 0.9944629  |
| C    | 0.99778516 | 0.9944629  | 0.00110742 | 0.99335548 | 0          |
| G    | 0          | 0.00221484 | 0          | 0          | 0.00110742 |
| T    | 0          | 0          | 0.9944629  | 0.00110742 | 0          |
| N    | 0          | 0          | 0          | 0          | 0          |
| -    | 0.00221484 | 0.00221484 | 0.00442968 | 0.00442968 | 0.00442968 |

**A very simple example that describes the code behaviour:**

```python
# Mergetable.windows.x86_64
$ cd test/
$ python C:\Users\DZ\Desktop\Mergetable\Mergetable.py -i samplelist.txt -n 
CRISPResso_quantification_of_editing_frequency -o out

$ python C:\Users\DZ\Desktop\Mergetable\Mergetable.py -i samplelist.txt -n Quantification_window_nucleotide_percentage_table -o out
```

```shell
# Mergetable.linux.x86_64
$ cd test/
$ Mergetable -i samplelist.txt -n CRISPResso_quantification_of_editing_frequency -o out
$ Mergetable -i samplelist.txt -n Quantification_window_nucleotide_percentage_table -o out

# test/
|-- CRISPResso_on_1
|   |-- CRISPResso_quantification_of_editing_frequency.txt
|   `-- Quantification_window_nucleotide_percentage_table.txt
|-- CRISPResso_on_2
|   |-- CRISPResso_quantification_of_editing_frequency.txt
|   `-- Quantification_window_nucleotide_percentage_table.txt
|-- CRISPResso_on_3
|   |-- CRISPResso_quantification_of_editing_frequency.txt
|   `-- Quantification_window_nucleotide_percentage_table.txt
|-- out
|   |-- CRISPResso_quantification_of_editing_frequency_Mergetable.csv
|   `-- Quantification_window_nucleotide_percentage_table_Mergetable.csv
`-- samplelist.txt

4 directories, 9 files
```


Run the example, and don't forget to watch it successfully!

```py
=================================
    Table Merged Successfully!

                    .---- .
                .       、
                _·'__       ·
            . --(o) (o)---/#\
        .`@             /###\
        :         ,     #####
        `-..__.-'  _.- \###/
            `;_:       `"
                .'""""""`.
                /,         \\
            //           \\
            `-._________.-'
                __`.|.`__
            (_____|_____)

=================================
```



## Manual

If you run into any problems, please contact me. https://github.com/ligeng-k/Mergetable
