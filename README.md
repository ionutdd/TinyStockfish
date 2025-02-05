# TinyStockfish

This project will represent my bachelor's degree thesis. 

TinyStockfish is a lightweight yet powerful chess engine written in C++. It focuses purely on search strength without relying on opening books or endgame tablebases. The goal is to achieve optimal move generation and evaluation efficiency using advanced search techniques. 

## Features
- **Bitboard Representation**: Efficient board state handling using `uint64_t`.
- **Move Generation**: Fast and legal move generation.
- **Alpha-Beta Pruning**: Enhanced minimax search with move ordering.
- **Quiescence Search**: Reduces horizon effect by exploring only meaningful captures.
- **Transposition Tables**: Caches previous search results for efficiency.
- **Iterative Deepening**: Helps optimize search with move ordering.
- **Evaluation Function**: Material balance, piece-square tables, and mobility heuristics.

## Project Structure
```
TinyStockfish/
│── src/
│   │── board.h / board.cpp       # Board representation
│   │── move.h / move.cpp         # Move structure and logic
│   │── move_generator.h / .cpp   # Legal move generation
│   │── search.h / search.cpp     # Alpha-beta pruning and enhancements
│   │── evaluation.h / .cpp       # Position evaluation
│   │── main.cpp                  # Entry point
│── tests/                        # Unit tests
│── README.md                     # This file
│── Makefile / CMakeLists.txt      # Build system
```

## Getting Started
### Prerequisites
- **C++17 or later**
- **CMake** (optional, for building)

### Build & Run
```
git clone https://github.com/yourusername/TinyStockfish.git
cd TinyStockfish
make  # Or use cmake
./tinystockfish
```

## Future Improvements
- Parallel search with multithreading.
- More advanced evaluation heuristics.
- Lazy SMP (parallel search optimization).
