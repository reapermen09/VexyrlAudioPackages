# VexyrlAudioPackages
Package Manager for Vexyrl Audio

API:

```cpp
void interpret(
    const std::vector<std::string>& code,
    std::vector<std::string>& instKeys, std::vector<std::string>& notes,
    std::vector<double>& starts, std::vector<double>& lengths,
    std::vector<double>& velocities, std::vector<double>& reverbs,
    std::vector<double>& pans, std::vector<double>& eqvlows,
    std::vector<double>& eqlows, std::vector<double>& eqmids,
    std::vector<double>& eqhighs, std::vector<double>& evhighs,
    std::vector<std::string>& revtypes, std::vector<double>& pitches,
    std::vector<double>& attacks, std::vector<double>& releases,
    std::vector<double>& tempos
); // YOU MUST CONVERT 'lengths' and 'starts' to beats!

const char* exportMidi(const std::vector<std::string>& code, int* outSize);

const char* getName();

const char* getDescription();
```
MIDI:

```

// by default, all midi channels are combined! you must seperate them!

// combined in the same channel!
midi Basic<Piano>[piano]
midi Basic<UprightPiano>[piano]
midi Lushreal<Piano>[piano]

// all different channels
midi Basic<Piano>[piano]
midi Basic<UprightPiano>[piano]+
midi Lushreal<Piano>[piano]+

// drums!

midi Basic<StandardDrums>[drum]

```

Your code is expected to follow these requirements before publishing!
