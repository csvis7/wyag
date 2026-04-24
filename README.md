# wyag - Write Yourself a Git!

A Python implementation of Git from scratch, built by following the [Write Yourself a Git](https://wyag.thb.lt) tutorial.

## What is this?

`wyag` is a simplified but **fully working** Git implementation in ~983 lines of pure Python. It implements all core Git commands and is **100% compatible** with real Git — objects created by wyag can be read by Git and vice versa.

## Commands Implemented

| Command | Description |
|---------|-------------|
| `wyag init` | Initialize a new repository |
| `wyag add` | Add files to the staging area |
| `wyag rm` | Remove files from the staging area |
| `wyag commit` | Record changes to the repository |
| `wyag status` | Show working tree status |
| `wyag log` | Display commit history as a Graphviz DAG |
| `wyag cat-file` | Display Git object contents |
| `wyag hash-object` | Hash a file into a Git object |
| `wyag ls-files` | List files in the staging area |
| `wyag ls-tree` | Pretty-print a tree object |
| `wyag checkout` | Checkout a commit into a directory |
| `wyag show-ref` | List all references |
| `wyag tag` | Create and list tags |
| `wyag rev-parse` | Resolve object names |
| `wyag check-ignore` | Check paths against ignore rules |

## What I Learned

- Git is a **content-addressed filesystem** — file names are SHA-1 hashes of their contents
- The commit history is a **Merkle DAG** — each commit is cryptographically bound to its entire history  
- The **index file** bridges the working tree and commits
- Git objects are **zlib-compressed** binary files with a simple header
- Branches are just **references** (text files containing a SHA-1 hash)

## How to Run

### Requirements
- Python 3.10+
- Linux / WSL2 / macOS

### Setup
```bash
git clone https://github.com/YOURUSERNAME/wyag.git
cd wyag
chmod +x wyag
```

### Usage
```bash
# Initialize a new repo
./wyag init myrepo

# Add and commit files
cd myrepo
echo "Hello" > hello.txt
../wyag add hello.txt
../wyag commit -m "first commit"

# Check status
../wyag status

# View history
../wyag log HEAD
```

## Tech Stack
- **Language:** Python 3.12
- **Environment:** WSL2 + VS Code
- **Platform:** Windows 11

## Credits
Based on the excellent [Write Yourself a Git](https://wyag.thb.lt) tutorial by Thibault Polge.
