# YAML Site Guide
## Using Site Data for Research and Documentation

**Version**: 1.0.0  
**Last Updated**: February 2026

---

## Table of Contents

1. [YAML Structure Overview](#yaml-structure-overview)
2. [Complete Tag Taxonomy](#complete-tag-taxonomy)
3. [Geographic Distribution](#geographic-distribution)
4. [Usage Examples](#usage-examples)
5. [Cross-Reference Matrix](#cross-reference-matrix)
6. [Tag Co-occurrence Patterns](#tag-co-occurrence-patterns)
7. [Quick Reference Tables](#quick-reference-tables)

---

## YAML Structure Overview

### Data Format

The site data is organized in a structured format with three primary components:

```
Site Name | Location | tags
```

**Components**:
1. **Site Name**: Official or commonly recognized name
2. **Location**: Geographic location (country/region, city/area)
3. **Tags**: Comma-separated classification tags

### Example Entries

```yaml
Great Pyramid of Giza | Egypt, Giza Plateau | precision_stonework, astronomical_alignment, monumental_scale, megalithic, pyramid
Sacsayhuamán | Peru, Cusco | polygonal_masonry, earthquake_resistant, massive_scale, knobs, weathering_stratification, multi_phase_construction
Barabar Caves | India, Bihar | mirror_polish, optical_quality, 3d_precision, acoustic_design, rock_cut, underground
Göbekli Tepe | Turkey, Şanlıurfa | pre_pottery_neolithic, earliest_temple, inverted_timeline, carving, astronomical_alignment
Puma Punku | Bolivia, Tiwanaku | modular_precision, h_block_design, andesite_difficulty, knobs, interior_channel_precision
```

### Data Fields Explained

**Site Name**:
- Official archaeological name preferred
- Common alternate names noted in documentation
- Consistent naming across repository

**Location**:
- Format: Country, Region/City
- Specific enough for identification
- Uses modern country names for clarity

**Tags**:
- Multiple tags per site (typically 3-8)
- Hierarchical from general to specific
- Consistent terminology across repository
- See [Complete Tag Taxonomy](#complete-tag-taxonomy) below

---

## Complete Tag Taxonomy

### Category 1: Construction Techniques

| Tag | Definition | Characteristics | Examples |
|-----|------------|-----------------|----------|
| `polygonal_masonry` | Irregularly-shaped interlocking stones fitted without mortar | Non-rectangular blocks, jigsaw-like fitting, paper-thin joints | Sacsayhuamán, Ollantaytambo, Delphi, Mycenae |
| `cyclopean_masonry` | Massive stone blocks without mortar (mythologically sized) | Blocks >20 tons, mortarless, rough-faced or fitted | Baalbek, Sacsayhuamán, Mycenae |
| `precision_fitting` | Joints so tight that paper/knife blade cannot fit between stones | <1mm joints, precision grinding/cutting, perfect planes | Sacsayhuamán, Puma Punku, Valley Temple, Western Stone |
| `precision_stonework` | Micron-to-millimeter level accuracy in dimensions/surfaces | Measured tolerances <1mm, often <100µm | Serapeum, predynastic vases, Barabar Caves, Puma Punku |
| `mortise_tenon_joinery` | Stones joined using projecting tenons fitting into mortise holes | Interlocking projections and recesses, no mortar needed | Stonehenge, Puma Punku H-blocks |
| `metal_clamps` | Metal connectors (bronze, copper, iron) joining stones | H-clamps, I-clamps, pour channels for molten metal | Ollantaytambo, Tiwanaku, Greek temples, Angkor Wat |
| `modular_construction` | Standardized, interchangeable components | Repeated dimensions, template-based, mass production | Puma Punku H-blocks, predynastic vases |
| `corner_first_construction` | Construction sequence where corners built first, then filled | Observable block types (corner, fill, taper), surveying from corners | Great Pyramid casing |
| `rock_cut` | Carved from living bedrock or cliff face | Subtraction method, no assembly, monolithic integration | Barabar Caves, Gal Vihara, Petra, Kailasa Temple |

### Category 2: Precision Levels

| Tag | Definition | Tolerance Range | Modern Equivalent | Examples |
|-----|------------|----------------|-------------------|----------|
| `micron_level_precision` | Dimensional/surface tolerances <100 microns | 0.001-0.100mm (1-100µm) | Precision CNC, surface grinding | Predynastic vases (15-50µm), Serapeum boxes (5µm) |
| `submillimeter_precision` | Tolerances between 0.1-1mm | 0.1-1.0mm (100-1000µm) | Standard CNC machining | Puma Punku interior channels (1mm) |
| `millimeter_precision` | Tolerances 1-10mm | 1-10mm | Professional machining/masonry | Puma Punku flat surfaces (1-2mm), Great Pyramid base (21mm over 230m) |
| `mirror_polish` | Surface finish approaching optical quality | Ra <1µm (surface roughness) | Optical polishing equipment | Barabar Caves (Ra<0.1µm), Serapeum boxes |
| `cnc_equivalent` | Precision requiring modern CNC to replicate today | Varies by artifact | 3-5 axis CNC, precision grinding | Predynastic vases, Serapeum boxes, Puma Punku H-blocks |
| `impossible_precision` | Precision exceeding expected capability by >10× | Context-dependent | Various advanced techniques | Predynastic vases (pre-hieroglyphic, pre-wheel), core drilling feed rates |

### Category 3: Site Types

| Tag | Definition | Characteristics | Examples |
|-----|------------|-----------------|----------|
| `stone_circle` | Circular arrangement of standing stones | Upright megaliths in circle, often astronomical alignment | Stonehenge, Avebury |
| `megalithic_alignment` | Linear or patterned arrangement of standing stones | Rows/patterns of menhirs, often kilometers long | Carnac Stones (France) |
| `passage_tomb` | Burial chamber accessed by passage, often under mound | Entrance passage, central chamber, corbelled vault | Newgrange, Knowth, Dowth |
| `dolmen` | Stone table structure (capstone on uprights) | Horizontal capstone on 3+ vertical stones, often burial | Carnac area, Korea, India |
| `temple` | Religious/ceremonial structure | Sacred architecture, ritual spaces, religious artifacts | Göbekli Tepe, Malta temples, Preah Vihear |
| `pyramid` | Pyramidal structure (stepped or smooth-sided) | Square/rectangular base, apex point, monumental scale | Great Pyramid, Pyramid of Sun, Mayan pyramids |
| `underground_temple` | Subterranean religious structure | Excavated below ground, religious function, carved chambers | Hypogeum of Ħal-Saflieni |
| `platform_mound` | Elevated artificial platform | Flat-topped earthwork, base for buildings/ceremonies | Cahokia Monks Mound, Tiwanaku Akapana |
| `effigy_mound` | Earthwork shaped like animal/figure | Recognizable shape from above, often enormous | Serpent Mound (Ohio), Great Serpent Mound (Canada) |
| `geoglyph` | Large ground design visible from above | Created by removing/arranging surface materials | Nazca Lines, Blythe Intaglios, Uffington White Horse |
| `stone_arrangement` | Pattern of stones (not circle/alignment) | Various arrangements, often astronomical/ceremonial | Aboriginal stone arrangements |

### Category 4: Engineering Features

| Tag | Definition | Significance | Examples |
|-----|------------|--------------|----------|
| `astronomical_alignment` | Aligned to solstice, equinox, or celestial events | Indicates astronomical knowledge, careful surveying | Stonehenge, Newgrange, Chankillo, Great Pyramid |
| `extreme_weight` | Individual blocks >100 tons | Exceptional transport/lifting challenge | Baalbek (1650t), Sacsayhuamán (200t), Puma Punku (130t) |
| `transport_mystery` | Long-distance or topographically difficult transport | Distance >10km OR significant elevation change | Stonehenge bluestones (250km), Ollantaytambo (900m elevation) |
| `monumental_scale` | Exceptional overall size/volume | Total volume >100,000 m³ or height >30m | Great Pyramid (2.3M blocks), Monks Mound (622,000 m³) |
| `carving` | Sculptural or relief carving in stone | Artistic/symbolic imagery, often intricate | Göbekli Tepe pillars, Malta temples, Angkor Wat |
| `acoustic_design` | Engineered acoustic properties | Resonance frequencies, amplification, specific echoes | Barabar Caves (110Hz), Hypogeum (110Hz) |
| `earthquake_resistant` | Design that withstands seismic activity | Polygonal masonry, flexible joints, multi-thousand-year survival | Sacsayhuamán, Machu Picchu, Japanese pagodas |
| `drainage_engineering` | Sophisticated water management systems | Channels, pipes, sewers, flood control | Mohenjo-Daro, Machu Picchu, Angkor Wat |

### Category 5: Tool Evidence

| Tag | Definition | Evidence Type | Examples |
|-----|------------|--------------|----------|
| `vitrification` | Glassy/heat-fused surfaces | Glass-like sheen, molecular fusion, heat evidence | Ollantaytambo, various Andean sites, Scottish vitrified forts |
| `core_drilling` | Evidence of rotary drilling | Circular holes, spiral grooves, feed rate evidence | Giza, Abu Gurab, Karnak, Aswan |
| `saw_marks` | Evidence of large saws cutting stone | Arc-shaped cuts, parallel striations, deep cuts | Giza, Abu Gurab, Abu Rawash |
| `scoop_marks` | Hemispherical depressions in stone | Curved concave depressions, often in quarries | Aswan quarries, Ollantaytambo |
| `knobs` | Protruding bosses on megalithic blocks | Cylindrical/conical protrusions, 5-20cm typical | Giza, Sacsayhuamán, Ollantaytambo, Puma Punku, Baalbek |
| `tool_marks` | General evidence of working methods | Percussion marks, abrasion patterns, shaping evidence | Various sites |

### Category 6: Material Types

| Tag | Definition | Mohs Hardness | Working Difficulty | Examples |
|-----|------------|--------------|-------------------|----------|
| `granite_work` | Working granite stone | 6-7 | Very difficult, harder than copper/bronze tools | Serapeum, Aswan obelisks, pyramid beams |
| `andesite_difficulty` | Working andesite stone | 6-7 | Very difficult, volcanic origin, hard and tough | Puma Punku, Ollantaytambo, Tiwanaku |
| `diorite_work` | Working diorite stone | 6.5-7 | Extremely difficult, very hard and dense | Predynastic vases, Egyptian statues |
| `basalt_work` | Working basalt stone | 6-7 | Very difficult, volcanic origin | Predynastic vases, paving stones |
| `limestone_work` | Working limestone | 3-4 | Moderate, softer and easier to work | Great Pyramid core, Baalbek, Valley Temple core |

### Category 7: Anomalies and Mysteries

| Tag | Definition | Implication | Examples |
|-----|------------|-------------|----------|
| `anomalous_age` | Dating problems or unexpectedly ancient | Challenges timeline of civilization development | Göbekli Tepe (9500 BCE pre-agriculture), Gunung Padang (20,000+ subsurface disputed) |
| `unknown_function` | Purpose unclear or heavily debated | Function not evident from structure/artifacts | Roman Dodecahedra, Cart Ruts of Malta, Yonaguni chambers |
| `technology_gap` | Capabilities exceed expected tech level for period | Suggests lost knowledge or underestimated capabilities | Antikythera Mechanism (1400 year gap), predynastic vases (pre-wheel) |
| `lost_technology` | Technique once mastered, now irreproducible | Process knowledge lost through time | Damascus steel formula, Greek fire, Roman concrete pozzolana |
| `dating_controversy` | Significant disagreement on age | Multiple dating methods give different results OR inscriptions vs. geological evidence | Sphinx water erosion, Serpent Mound, Gunung Padang subsurface |
| `uninscribed_precision` | High precision work with no inscriptions/hieroglyphs | Complicates attribution and dating | Serapeum boxes, Osireion, predynastic vases |
| `weathering_paradox` | Weathering inconsistent with attributed age | Geological weathering suggests earlier date than inscriptions | Valley Temple, Sphinx, Osireion |
| `multi_phase_construction` | Observable quality degradation over building phases | Earliest = most sophisticated, contradicts expected development | Sacsayhuamán, Giza complex, Malta temples, Göbekli Tepe |
| `inverted_timeline` | Oldest layer = most sophisticated (opposite of expected) | Challenges linear technological progression assumption | Göbekli Tepe Layer III, construction phases pattern globally |
| `transport_mystery` | Movement of materials unexplained by known methods | Distance, weight, or terrain makes transport puzzling | Stonehenge bluestones, Baalbek trilithon movement to height |

### Category 8: Specific Features

| Tag | Definition | Significance | Examples |
|-----|------------|--------------|----------|
| `h_block_design` | H-shaped stone blocks with interior cuts | Modular precision, standardized design, unknown function | Puma Punku |
| `interior_channel_precision` | Precise channels/grooves carved inside blocks | Indicates advanced cutting tools or techniques | Puma Punku (1mm tolerance) |
| `handle_problem` | Integral handles geometrically incompatible with lathe | Challenges conventional manufacturing explanations | Predynastic vases with curved handles |
| `optical_quality` | Surface finish at optical/mirror quality | Requires extreme polishing precision | Barabar Caves |
| `3d_precision` | Precision maintained in all three dimensions | Not just flat surfaces but complex 3D geometries | Barabar Caves chambers, predynastic vases |
| `mass_production` | Evidence of large-scale standardized production | Thousands of similar artifacts with consistent quality | Predynastic vases (30,000+ in early dynastic period) |
| `weathering_stratification` | Multiple weathering layers showing construction phases | Quantifiable weathering differences between phases | Sacsayhuamán (5-15mm oldest vs 0.5-2mm newest) |
| `weathering_within_cuts` | Weathering inside precision cuts, proving cut is original | Rules out later cutting of pre-weathered blocks | Puma Punku precision cuts |

### Category 9: Geographic/Cultural Patterns

| Tag | Definition | Significance | Examples |
|-----|------------|--------------|----------|
| `egypt_peru_parallel` | Similar features in Egypt and Peru despite no known contact | Suggests either convergent evolution or diffused knowledge | Polygonal masonry, precision stonework, knobs, scoop marks |
| `global_megalithic` | Similar megalithic practices across multiple continents | Universal human response to similar challenges? | Stone circles, dolmens, menhirs across Europe, Asia, Americas |
| `cross_cultural_consistency` | Remarkably similar techniques across unconnected cultures | Particularly striking when precision/dimensions are consistent | Knobs (Egypt, Peru, Bolivia), polygonal masonry worldwide |
| `pre_pottery_neolithic` | Predates pottery and often agriculture | Challenges assumptions about what hunter-gatherers could achieve | Göbekli Tepe (9500 BCE) |
| `pre_hieroglyphic` | Predates invention of hieroglyphic writing in Egypt | Makes attribution and dating challenging | Predynastic vases (3600-3100 BCE), Sphinx (if early date correct) |

---

## Geographic Distribution

### Site Density by Region

| Region | Number of Major Sites | Primary Anomaly Types | Time Period Range |
|--------|---------------------|---------------------|-------------------|
| **Egypt** | 10+ | Precision stonework, extreme transport, micron tolerances, core drilling | 3600 BCE - 300 BCE |
| **Peru** | 5+ | Polygonal masonry, megalithic scale, vitrification, knobs | 200 BCE - 1500 CE |
| **Bolivia** | 2 | Modular precision, H-blocks, andesite work, interior channels | 536-600 CE (traditional) |
| **Turkey** | 1 | Pre-agricultural monuments, inverted timeline | 9500-8800 BCE |
| **Lebanon** | 1 | Extreme weight (1650 tons), submillimeter tolerances | Unknown (Roman period traditional) |
| **Malta** | 3 | Underground temples, acoustic design, megalithic structures | 3600-2500 BCE |
| **England/Ireland** | 3 | Long-distance transport, astronomical alignment | 3000-1600 BCE |
| **France** | 2 | Megalithic alignments, extensive stone rows | 4500-3300 BCE |
| **India** | 3+ | Mirror polish, optical quality surfaces, rock carving | 3rd century BCE - 12th century CE |
| **Greece** | 2 | Mechanical complexity, lost technology, rock carving | 150 BCE - 200 BCE |
| **Easter Island** | 1 | Monolithic statues, transport mystery | 1250-1500 CE |
| **North America** | 6+ | Earthworks, effigy mounds, geoglyphs | 1650 BCE - 1200 CE |

### Continental Breakdown

**Africa**: 12+ sites
- Dominated by Egyptian precision stonework and megalithic transport
- Concentration in Nile Valley and Aswan area
- Time depth: 3600 BCE to Late Period

**Asia**: 10+ sites
- Diverse: from mirror polish (India) to mechanical complexity (Greece) to pre-agricultural monuments (Turkey)
- Spread across Middle East, South Asia, Southeast Asia
- Time depth: 9500 BCE to 12th century CE

**Europe**: 8+ sites
- Dominated by megalithic monuments (stone circles, alignments, dolmens)
- Atlantic facade concentration (France, Britain, Ireland, Malta)
- Time depth: 4500 BCE to Roman period

**South America**: 7+ sites
- Concentrated in Andean region (Peru, Bolivia)
- Polygonal masonry and extreme precision focus
- Time depth: 200 BCE to Spanish conquest

**North America**: 6+ sites
- Dominated by earthwork/mound builders
- Concentrated in Mississippi Valley and Eastern Woodlands
- Time depth: 1650 BCE to European contact

**Oceania**: 1 major site (Easter Island)
- Unique monolithic statue tradition
- Time depth: 1250-1500 CE

---

## Usage Examples

### Query 1: Find All Sites with Precision Stonework

**Tags to search**: `precision_stonework`, `micron_level_precision`, `submillimeter_precision`, `mirror_polish`

**Results**:
- Serapeum of Saqqara (Egypt) - micron_level_precision, mirror_polish
- Predynastic Vases (Egypt) - micron_level_precision, cnc_equivalent
- Barabar Caves (India) - mirror_polish, optical_quality, 3d_precision
- Puma Punku (Bolivia) - modular_precision, submillimeter_precision, interior_channel_precision
- Great Pyramid (Egypt) - precision_stonework, millimeter_precision (base leveling)

**Documentation**: See precision-stonework.md, predynastic-vases.md

### Query 2: Find All Sites with Polygonal Masonry

**Tags to search**: `polygonal_masonry`

**Results**:
- Sacsayhuamán (Peru)
- Ollantaytambo (Peru)
- Delphi (Greece)
- Mycenae (Greece)
- Megalithic Wall of Arwad (Syria)

**Common co-occurring tags**: `earthquake_resistant`, `precision_fitting`, `knobs`, `multi_phase_construction`

**Documentation**: See megalithic-engineering.md, construction-phases.md

### Query 3: Find Sites Showing Inverted Timeline Pattern

**Tags to search**: `inverted_timeline`, `multi_phase_construction`, `weathering_stratification`

**Results**:
- Göbekli Tepe (Turkey) - inverted_timeline, Layer III oldest and most sophisticated
- Sacsayhuamán (Peru) - multi_phase_construction, weathering_stratification, largest blocks in oldest layer
- Giza Complex (Egypt) - multi_phase_construction, weathering_paradox
- Malta Temples - multi_phase_construction
- Easter Island - cultural_collapse, largest moai unfinished

**Pattern**: Oldest = most sophisticated, degradation over time

**Documentation**: See construction-phases.md

### Query 4: Find All Sites with Extreme Weights (>100 tons)

**Tags to search**: `extreme_weight`

**Results**:
- Baalbek (Lebanon) - 1650 tons (Stone of Pregnant Woman), 800-1200 tons (Trilithon)
- Sacsayhuamán (Peru) - 120-200 tons
- Puma Punku (Bolivia) - 130-180 tons
- Serapeum (Egypt) - ~100 tons per box with lid

**Common challenges**: Transport, lifting, precision placement

**Documentation**: See megalithic-engineering.md

### Query 5: Find All Pre-Agricultural Sites

**Tags to search**: `pre_pottery_neolithic`, `anomalous_age`

**Results**:
- Göbekli Tepe (Turkey) - 9500-8800 BCE, pre-pottery, pre-agriculture
- Poverty Point (USA) - 1650-700 BCE, hunter-gatherer society

**Significance**: Challenges assumptions about complexity requiring agriculture

**Documentation**: See ancient-knowledge.md, megalithic-engineering.md

### Query 6: Find Sites with Egyptian-Peruvian Parallels

**Tags to search**: `egypt_peru_parallel`, sites in both Egypt and Peru/Bolivia

**Parallel Features**:
- **Polygonal Masonry**: Egypt (Valley Temple, Sphinx Temple) vs. Peru (Sacsayhuamán, Ollantaytambo)
- **Knobs**: Egypt (Giza, Aswan) vs. Peru (Sacsayhuamán, Ollantaytambo) vs. Bolivia (Puma Punku, Tiwanaku)
- **Precision Stonework**: Egypt (Serapeum, vases) vs. Bolivia (Puma Punku)
- **Scoop Marks**: Egypt (Aswan quarries) vs. Peru (Ollantaytambo)
- **Megalithic Scale**: Both regions work with 100+ ton blocks

**Controversy**: Convergent evolution vs. diffusion vs. common ancestor culture

**Documentation**: See knobs.md, scoop-marks.md, construction-phases.md

### Query 7: Find All Acoustic Design Features

**Tags to search**: `acoustic_design`

**Results**:
- Barabar Caves (India) - 110Hz resonance, amplification
- Hypogeum of Ħal-Saflieni (Malta) - 110Hz resonance

**Significance**: Same resonance frequency (110Hz) in unconnected cultures

**Research interest**: Were these frequencies chosen for specific effects? (110Hz affects human brain patterns)

**Documentation**: See megalithic-engineering.md, precision-stonework.md

---

## Cross-Reference Matrix

### Feature Type → Sites → Documentation

| Feature Type | Primary Sites | Secondary Sites | Documentation Files |
|-------------|---------------|----------------|-------------------|
| **Micron-Level Precision** | Predynastic vases, Serapeum boxes, Barabar Caves | Puma Punku | precision-stonework.md, predynastic-vases.md, inscription-dating-problem.md |
| **Polygonal Masonry** | Sacsayhuamán, Ollantaytambo | Delphi, Mycenae, Arwad | megalithic-engineering.md, construction-phases.md |
| **Extreme Weight (>500t)** | Baalbek | Sacsayhuamán (largest blocks) | megalithic-engineering.md |
| **Core Drilling** | Giza, Abu Gurab, Karnak | Aswan | precision-stonework.md |
| **Saw Marks** | Giza, Abu Gurab, Abu Rawash | Various Egyptian sites | precision-stonework.md |
| **Knobs** | Giza, Sacsayhuamán, Ollantaytambo, Puma Punku | Baalbek, Tiwanaku | knobs.md, stone-softening-hypothesis.md |
| **Scoop Marks** | Aswan quarries, Ollantaytambo | Puma Punku, Tiwanaku | scoop-marks.md, stone-softening-hypothesis.md |
| **Inverted Timeline** | Göbekli Tepe | Sacsayhuamán, Giza complex, Malta temples | construction-phases.md |
| **Inscription Dating Problem** | Serapeum, Valley Temple, Osireion | Sphinx, Great Pyramid | inscription-dating-problem.md, construction-phases.md |
| **Astronomical Alignment** | Stonehenge, Newgrange, Chankillo | Great Pyramid, Carnac, Nazca Lines | ancient-knowledge.md, geoglyphs.md |
| **Geoglyphs** | Nazca Lines, Carnac Stones | Uffington White Horse, Blythe Intaglios | geoglyphs.md |
| **Mirror Polish** | Barabar Caves, Serapeum boxes | - | precision-stonework.md |
| **Acoustic Design** | Barabar Caves, Hypogeum | - | megalithic-engineering.md |
| **Modular Construction** | Puma Punku H-blocks | Predynastic vases | precision-stonework.md, predynastic-vases.md |

### Documentation File → Primary Sites Covered

| Documentation File | Primary Sites | Focus Areas |
|-------------------|---------------|-------------|
| **megalithic-engineering.md** | Baalbek, Great Pyramid, Sacsayhuamán, Stonehenge, Puma Punku, Ollantaytambo, Easter Island, Carnac, Göbekli Tepe, Mohenjo-Daro, Malta Temples, Hypogeum, Cahokia | Transport, lifting, massive scale |
| **precision-stonework.md** | Serapeum, Predynastic vases, Barabar Caves, Puma Punku, Core drilling sites, Saw mark sites, Western Stone, Cart Ruts, Rock-cut sites | Micron-level accuracy, surface finishes, tolerances |
| **ooparts.md** | Antikythera Mechanism, Baghdad Battery, various controversial artifacts | Anachronistic technology, debunked claims |
| **ancient-knowledge.md** | Göbekli Tepe, Piri Reis Map, astronomical sites, Antikythera Mechanism | Advanced ancient knowledge, astronomy, mathematics |
| **geoglyphs.md** | Nazca Lines, Carnac Stones, Uffington White Horse, Cahokia, Serpent Mound, various earthworks | Large-scale ground designs, aerial perspective |
| **construction-phases.md** | Göbekli Tepe, Sacsayhuamán, Giza complex, Malta temples, Easter Island, Stonehenge | Degradation pattern, inverted timeline, weathering |
| **inscription-dating-problem.md** | Serapeum, Valley Temple, Osireion, Sphinx, Great Pyramid, Predynastic vases | Dating methodology, uninscribed precision, weathering differential |
| **predynastic-vases.md** | Predynastic Egyptian vases | Extreme precision, handle problem, machine-tool paradox |
| **knobs.md** | Giza, Sacsayhuamán, Ollantaytambo, Puma Punku, Tiwanaku, Baalbek | Protruding bosses, cross-cultural consistency |
| **scoop-marks.md** | Aswan quarries, Ollantaytambo, Puma Punku | Hemispherical depressions, quarrying techniques |
| **pyramid-casing-construction.md** | Great Pyramid | Corner-first construction, 8-sided geometry, internal ramp theory |

---

## Tag Co-occurrence Patterns

### High Co-occurrence Pairs (Frequently Occur Together)

| Primary Tag | Frequently Co-occurs With | Sites Exhibiting Both | Interpretation |
|------------|--------------------------|---------------------|----------------|
| `polygonal_masonry` | `precision_fitting` | Sacsayhuamán, Ollantaytambo, Delphi | Polygonal masonry requires precision fitting |
| `polygonal_masonry` | `earthquake_resistant` | Sacsayhuamán, Ollantaytambo | Flexible joints provide earthquake resistance |
| `polygonal_masonry` | `knobs` | Sacsayhuamán, Ollantaytambo | Knobs appear on largest polygonal blocks |
| `extreme_weight` | `transport_mystery` | Baalbek, Sacsayhuamán, Stonehenge | Heaviest stones pose transport challenges |
| `micron_level_precision` | `uninscribed_precision` | Serapeum boxes, Predynastic vases | Highest precision artifacts lack inscriptions |
| `micron_level_precision` | `cnc_equivalent` | Serapeum boxes, Predynastic vases, Puma Punku | Micron precision requires CNC-equivalent today |
| `mirror_polish` | `acoustic_design` | Barabar Caves, Hypogeum (partially) | Polished surfaces in acoustic chambers |
| `mirror_polish` | `granite_work` | Barabar Caves, Serapeum boxes | Mirror polish achieved on hardest stones |
| `multi_phase_construction` | `weathering_paradox` | Giza complex, Sacsayhuamán | Multiple phases show differential weathering |
| `multi_phase_construction` | `weathering_stratification` | Sacsayhuamán | Quantifiable weathering differences by phase |
| `knobs` | `precision_fitting` | Sacsayhuamán, Puma Punku | Knobs on most precisely fitted blocks |
| `knobs` | `megalithic` | Giza, Sacsayhuamán, Baalbek | Knobs on largest blocks |
| `astronomical_alignment` | `temple` | Stonehenge, Newgrange, Göbekli Tepe (debated) | Religious sites often aligned astronomically |
| `underground_temple` | `acoustic_design` | Hypogeum | Underground chambers enhance acoustics |
| `inverted_timeline` | `multi_phase_construction` | Göbekli Tepe, Sacsayhuamán | Degradation over phases creates inverted timeline |

### Tag Clustering (Groups of Tags That Often Appear Together)

**Precision Engineering Cluster**:
- `micron_level_precision` + `uninscribed_precision` + `cnc_equivalent` + `mirror_polish`
- Sites: Serapeum boxes, Predynastic vases, Barabar Caves
- Interpretation: Highest precision work lacks attribution

**Andean Megalithic Cluster**:
- `polygonal_masonry` + `earthquake_resistant` + `knobs` + `multi_phase_construction` + `precision_fitting`
- Sites: Sacsayhuamán, Ollantaytambo, Machu Picchu
- Interpretation: Distinctive Andean construction style

**Ancient Knowledge Cluster**:
- `astronomical_alignment` + `temple` + `anomalous_age`
- Sites: Göbekli Tepe, Stonehenge, Newgrange
- Interpretation: Ancient astronomical sophistication

**Dating Problem Cluster**:
- `uninscribed_precision` + `weathering_paradox` + `multi_phase_construction` + `dating_controversy`
- Sites: Serapeum, Valley Temple, Osireion, Sphinx
- Interpretation: Attribution and dating challenges

**Egypt-Peru Parallel Cluster**:
- `polygonal_masonry` + `knobs` + `precision_fitting` + `megalithic`
- Sites: Valley Temple (Egypt), Sacsayhuamán (Peru), Ollantaytambo (Peru)
- Interpretation: Cross-cultural similarities

---

## Quick Reference Tables

### Table 1: Sites by Precision Level

| Precision Level | Sites | Measured Precision | Modern Equivalent |
|----------------|-------|-------------------|-------------------|
| **<50 microns** | Predynastic vases (15-50µm), Serapeum boxes (5µm) | 5-50µm | Precision CNC, surface grinder |
| **50-500 microns** | Barabar Caves (Ra <0.1µm = surface roughness) | 0.1-0.5µm Ra | Optical polishing |
| **0.5-2mm** | Puma Punku flat surfaces, interior channels | 0.5-2mm | Standard CNC machining |
| **2-10mm** | Great Pyramid base leveling, various megalithic joints | 2-10mm | Professional masonry |
| **1-5cm** | Polygonal masonry joints, most megalithic fitting | 10-50mm | Skilled hand masonry |

### Table 2: Sites by Weight Category

| Weight Category | Sites | Heaviest Block | Total Structure |
|----------------|-------|----------------|----------------|
| **>1000 tons** | Baalbek | 1650 tons (Stone of Pregnant Woman) | Multiple 800-1200 ton blocks |
| **500-1000 tons** | Western Stone (Jerusalem) | 570 tons | Single block in wall |
| **200-500 tons** | Sacsayhuamán | 120-200 tons (largest blocks) | Hundreds of 50-200 ton blocks |
| **100-200 tons** | Puma Punku, Serapeum | 130-180 tons (platform), ~100 tons (boxes) | Multiple 100+ ton pieces |
| **50-100 tons** | Great Pyramid, Ollantaytambo | 80 tons (granite beams), 50-70 tons (monoliths) | Thousands of multi-ton blocks |

### Table 3: Sites by Age (Oldest to Newest)

| Time Period | Sites | Significance |
|------------|-------|--------------|
| **9500-8800 BCE** | Göbekli Tepe | Earliest known temple, pre-agriculture |
| **4500-3300 BCE** | Carnac Stones | Largest megalithic site |
| **3600-3100 BCE** | Predynastic vases, Malta temples, Hypogeum | Pre-hieroglyphic precision, earliest free-standing structures |
| **3000-1600 BCE** | Stonehenge | Bluestone transport mystery |
| **2560 BCE** | Great Pyramid | Largest pyramid, extreme precision |
| **300 BCE-600 CE** | Serapeum, Puma Punku, Nazca Lines | Precision granite boxes, modular H-blocks, geoglyphs |
| **150-100 BCE** | Antikythera Mechanism | 1400-year technology gap |
| **536-600 CE** | Tiwanaku (traditional dating) | Andean megalithic center |
| **900-1200 CE** | Cahokia | Largest pre-Columbian North American city |
| **1200-1500 CE** | Inca sites (traditional), Easter Island moai | Latest megalithic traditions |

### Table 4: Tag Frequency Across All Sites

| Tag | Frequency | Percentage | Primary Examples |
|-----|-----------|-----------|-----------------|
| `precision_fitting` | High | ~40% of sites | Sacsayhuamán, Puma Punku, Serapeum, Valley Temple |
| `megalithic` | High | ~60% of sites | Most sites with blocks >20 tons |
| `astronomical_alignment` | Medium | ~30% of sites | Stonehenge, Newgrange, Great Pyramid, Chankillo |
| `multi_phase_construction` | Medium | ~25% of sites | Sacsayhuamán, Giza complex, Malta temples |
| `polygonal_masonry` | Low-Medium | ~15% of sites | Sacsayhuamán, Ollantaytambo, Delphi, Mycenae |
| `micron_level_precision` | Low | ~8% of sites | Predynastic vases, Serapeum boxes, Barabar Caves |
| `knobs` | Low | ~12% of sites | Giza, Sacsayhuamán, Ollantaytambo, Puma Punku, Baalbek |
| `extreme_weight` | Low | ~10% of sites | Baalbek, Sacsayhuamán, Puma Punku, Serapeum |

### Table 5: Research Priority by Anomaly Strength

| Priority Level | Criteria | Sites | Why High Priority |
|---------------|----------|-------|------------------|
| **Critical** | Quantified precision <100µm + peer-reviewed | Predynastic vases, Serapeum boxes, Barabar Caves | Measurable, verifiable, extreme anomalies |
| **Critical** | Rigorous dating + inverted timeline | Göbekli Tepe | Challenges civilization timeline fundamentally |
| **High** | Extreme weight >500 tons + verified | Baalbek, Sacsayhuamán (largest) | Transport/lifting mystery at extreme scale |
| **High** | Cross-cultural consistency with dimensional match | Knobs (Egypt-Peru-Bolivia) | Suggests connection or convergence, quantifiable |
| **Medium** | Well-documented but explainable anomalies | Stonehenge bluestone transport | Impressive but within extended human capability |
| **Medium** | Astronomical alignments with calculation precision | Stonehenge, Chankillo, Newgrange | Shows ancient knowledge sophistication |
| **Low** | Debated natural vs. artificial | Yonaguni Monument, Bimini Road | Fundamental question unresolved |
| **Avoid** | Debunked or hoaxes | Crystal skulls, Coso artifact, Dropa stones | Waste of research time |

---

## Conclusion

This YAML Site Guide provides a structured framework for:
1. **Classifying sites** by construction technique, precision level, site type, features, and anomalies
2. **Querying sites** by tags to find related examples
3. **Understanding patterns** through tag co-occurrence analysis
4. **Prioritizing research** based on anomaly strength and verification
5. **Cross-referencing** sites with documentation files

### Best Practices for Using This Guide:

1. **Start with tags** - Identify relevant classification tags for your research
2. **Query systematically** - Use tag combinations to find related sites
3. **Cross-reference documentation** - Connect sites to detailed analysis files
4. **Note co-occurrences** - Understand which features appear together
5. **Assess priorities** - Focus on high-priority, well-documented anomalies
6. **Maintain consistency** - Use standardized tags across all research

### Integration with Other AI Instructions:

- **ai-agent-reference.md**: Detailed site descriptions and research protocols
- **ai-research-methodology.md**: How to evaluate and research claims
- **html-conversion-instructions.md**: How to present data visually

---

**Document Version**: 1.0.0  
**Maintained By**: Repository contributors  
**Last Review**: February 2026  
**Next Review**: As needed based on new site discoveries
