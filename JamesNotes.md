My notes 5/22/2025


DefectHunter: Creates a deep-learning model that is used to detect vulnerabilities.

build: Holds the core compiled code of the deep learning model 

data/raw: This data was gathered using the web scraper, still needs to be converted to alpaca format so it can be fed to the model. 

network/pycache: holds the compiled code

network/attention.py: Contains the position embedding and sinusoidal position embedding classes

network/network.py: Contains the multi-head self-attention class, feed-forward network, ConformerEncoderBlock, ConformerEncoder, Transformer Block, and Token Position Embedding

process/unx/config.json: Config for the transformer

process/unx/merges.txt: Holds subword tokenization

process/build_ast.py: Gets the code snippet, converts to an AST then converts AST to dot then matrix

process/build_cfgdfg.py: Holds the build components for the cfg and dfg files

process/build_pls.py: tokenizes the raw json data and saves to a numpy file

process/build_y.py: Creates the array and prints the shape of it

process/Specialword.py: Creates roberta tokens

process/unixcoder.py: Holds all the tokenization code



Dependencies:

External Modules: Keras, tensorflow, numpy, Graphviz, tree_sitter, torch, unixcoder, nltk

Physical Requirements: 320gb ram, NVIDIA A40 GPU {48gb VRAM} x4, AMD EPYC 7543 32 core x2,

Data: Collected from the Common Weakness Enumeration Specification with 77 different vulnerabilities. Gathered the code examples of the CVE instances mentioned from the National Vulnerability Database using a web crawler. Data divided into vulnerability indicator, associated programming language, contextual description