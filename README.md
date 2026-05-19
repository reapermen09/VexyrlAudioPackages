# VexyrlAudioPackages
Package Manager for Vexyrl Audio

API:

```cpp
void interpret(
    const std::vector<std::string>& code,
    std::vector<std::string>& instKeys,
    std::vector<std::string>& notes,
    std::vector<double>& startBeats,
    std::vector<double>& lengthBeats,
    std::vector<double>& velocities,
    std::vector<double>& reverbs,
    std::vector<double>& pans,
    std::vector<double>& eqvlows,
    std::vector<double>& eqlows,
    std::vector<double>& eqmids,
    std::vector<double>& eqhighs,
    std::vector<double>& evhighs,
    std::vector<std::string>& revtypes,
    std::vector<double>& pitches,
    std::vector<double>& attackBeats,
    std::vector<double>& releaseBeats,
    std::vector<double>& tempos
);

const char* exportMidi(const std::vector<std::string>& code, int* outSize);
// returns data

const char* getName();
// returns name

const char* getDescription();
// returns description

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

// Piano and Upright piano in same channel, Lushreal Piano in a different one!
midi Basic<Piano>[piano]
midi Basic<UprightPiano>[piano]
midi Lushreal<Piano>[piano]+

// drums!

midi Basic<StandardDrums>[drum]

```

Your code is expected to follow these requirements before publishing!
