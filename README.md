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

// Piano and Upright piano in same channel, Lushreal Piano in a different one!
midi Basic<Piano>[piano]
midi Basic<UprightPiano>[piano]
midi Lushreal<Piano>[piano]+

// drums!

midi Basic<StandardDrums>[drum]

```

MIDI DEFINITIONS:

```cpp

static const std::vector<Entry> map = {
    {"acoustic grand", 0}, {"bright piano", 1}, {"electric grand", 2},
    {"honky", 3}, {"epiano", 4}, {"electric piano", 4},
    {"electric piano 2", 5}, {"harpsichord", 6}, {"clavinet", 7},
    {"celesta", 8}, {"glockenspiel", 9}, {"music box", 10},
    {"vibraphone", 11}, {"marimba", 12}, {"xylophone", 13},
    {"tubular bell", 14}, {"dulcimer", 15},
    {"drawbar organ", 16}, {"percussive organ", 17},
    {"rock organ", 18}, {"church organ", 19},
    {"reed organ", 20}, {"accordion", 21},
    {"harmonica", 22}, {"bandoneon", 23},
    {"nylon guitar", 24}, {"acoustic guitar", 24},
    {"steel guitar", 25},
    {"jazz guitar", 26}, {"clean guitar", 27},
    {"muted guitar", 28}, {"overdrive guitar", 29},
    {"distortion guitar", 30}, {"guitar harmonic", 31},
    {"acoustic bass", 32}, {"finger bass", 33},
    {"picked bass", 34}, {"fretless bass", 35},
    {"slap bass", 36}, {"slap bass 2", 37},
    {"synth bass", 38}, {"synth bass 2", 39},
    {"violin", 40}, {"viola", 41}, {"cello", 42},
    {"contrabass", 43}, {"tremolo string", 44},
    {"pizz", 45}, {"pizzicato", 45},
    {"harp", 46}, {"timpani", 47},
    {"string ensemble", 48}, {"strings", 48},
    {"string ensemble 2", 49},
    {"synth string", 50}, {"synth strings", 50},
    {"choir", 52}, {"voice", 52},
    {"doo", 53}, {"vox", 53},
    {"orchestra hit", 55},
    {"trumpet", 56}, {"trombone", 57}, {"tuba", 58},
    {"muted trumpet", 59},
    {"french horn", 60}, {"horn", 60},
    {"brass section", 61}, {"brass", 61},
    {"synth brass", 62}, {"synth brass 2", 63},
    {"soprano sax", 64}, {"alto sax", 65},
    {"tenor sax", 66}, {"baritone sax", 67},
    {"sax", 65},
    {"oboe", 68}, {"english horn", 69},
    {"bassoon", 70}, {"clarinet", 71},
    {"piccolo", 72}, {"flute", 73},
    {"recorder", 74}, {"pan flute", 75},
    {"blown bottle", 76}, {"shakuhachi", 77},
    {"whistle", 78}, {"ocarina", 79},
    {"lead", 80}, {"square", 80}, {"saw", 81},
    {"calliope", 82}, {"chiff", 83},
    {"charang", 84}, {"voice lead", 85},
    {"fifths", 86}, {"bass lead", 87},
    {"pad", 88}, {"new age", 88},
    {"warm pad", 89}, {"polysynth", 90},
    {"choir pad", 91}, {"bowed pad", 92},
    {"metallic pad", 93}, {"halo pad", 94},
    {"sweep pad", 95},
    {"rain", 96}, {"soundtrack", 97},
    {"crystal", 98}, {"atmosphere", 99},
    {"brightness", 100}, {"goblins", 101},
    {"echo", 102}, {"sci-fi", 103},
    {"sitar", 104}, {"banjo", 105},
    {"shamisen", 106}, {"koto", 107},
    {"kalimba", 108}, {"bagpipe", 109},
    {"fiddle", 110}, {"shanai", 111},
    {"tinkle bell", 112}, {"agogo", 113},
    {"steel drum", 114}, {"woodblock", 115},
    {"taiko", 116}, {"melodic tom", 117},
    {"synth drum", 118}, {"reverse cymbal", 119}
};

```

Your code is expected to follow these requirements before publishing!
