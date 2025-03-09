# Split Keyboards Dataset

A comprehensive dataset of split mechanical keyboards, featuring 187 different models with detailed specifications and features. This dataset combines information from multiple sources to provide a unified reference for mechanical keyboard enthusiasts, ergonomic computing advocates, and keyboard makers.

## Dataset Overview

This CSV file contains detailed information about split mechanical keyboards, including ergonomic, ortholinear, and traditional split designs. The dataset covers commercial products, DIY kits, and community designs from the mechanical keyboard ecosystem.

## Data Structure

The dataset contains the following fields:

| Field | Description | Example Values |
|-------|-------------|----------------|
| id | Unique identifier for the keyboard | `corne`, `ergodox`, `moonlander` |
| name | Full name of the keyboard | `Corne (CRKBD)`, `ErgoDox EZ`, `Moonlander Mark I` |
| brand | Manufacturer or creator | `ZSA`, `Keebio`, `foostan` |
| productPageUrl | Primary website or product page | `https://ergodox-ez.com` |
| otherUrls | Additional URLs (pipe-separated) | `https://github.com/qmk/qmk_firmware/tree/master/keyboards/iris` |
| images | URLs to product images (pipe-separated) | `https://raw.githubusercontent.com/diimdeep/awesome-split-keyboards/master/img/Corne.jpg` |
| releaseDate | Approximate release date (YYYY-MM-DD) | `2019-01-01` |
| isWireless | Supports wireless connectivity | `true`, `false` |
| isOpenSource | Has open-source hardware/firmware | `true`, `false` |
| isMechanical | Uses mechanical switches | `true`, `false` |
| isHotSwappable | Supports hot-swappable switches | `true`, `false` |
| hasDisplay | Has display (typically OLED) | `true`, `false` |
| hasRotaryEncoder | Includes rotary encoder(s) | `true`, `false` |
| hasNumberRow | Has dedicated number row | `true`, `false` |
| isTentable | Supports tenting/tilting | `true`, `false` |
| hasBacklight | Has key backlighting | `true`, `false` |
| hasPerKeyRGB | Has per-key RGB lighting | `true`, `false` |
| keyCount | Number of keys (or range) | `42`, `60-65` |
| staggerType | Key arrangement pattern | `column`, `row`, `ortholinear` |
| switchType | Compatible switch types (pipe-separated) | `MX`, `Choc`, `MX|Choc` |
| firmware | Supported firmware (pipe-separated) | `QMK`, `ZMK`, `QMK|ZMK` |
| buildType | Assembly/availability type | `diy`, `prebuilt`, `both` |
| notes | Additional information | `Popular 42-key split keyboard with OLED displays...` |

## Missing Data

Missing or unknown data is represented by a dash (`-`) in the CSV. This occurs for several reasons:

1. **Information not available** - Many DIY or community-designed keyboards have limited documentation, especially for older or niche designs.

2. **Subjective or variable features** - Some features might be added by users as mods, or might be present in some versions but not others.

3. **Discontinued products** - Historical keyboards may have limited information available online.

4. **Custom/personal designs** - Some keyboards are one-off or small-batch projects with minimal documentation.

Fields that most commonly have missing data:
- `releaseDate` - Often not clearly documented for community projects
- `hasDisplay`, `isHotSwappable`, `hasBacklight` - These features vary between builds for DIY keyboards
- `isTentable` - Support for tenting may depend on custom cases

## Data Sources

This dataset was compiled from:
- The [awesome-split-keyboards](https://github.com/diimdeep/awesome-split-keyboards) repository
- Community repositories and forums
- Official product pages
- QMK firmware repository listings
- Community databases

## Usage Examples

This dataset can be used for:

- Finding keyboards that match specific criteria (e.g., wireless + hotswap)
- Comparing features across different models
- Historical analysis of split keyboard evolution
- Generating visualizations of the split keyboard landscape
- Powering keyboard selection tools or recommendation engines

## Importing the Data

The data is provided in CSV format for maximum compatibility. You can import it using:

```python
# Python example with pandas
import pandas as pd
keyboards_df = pd.read_csv('split_keyboards.csv')

# Filter for wireless keyboards with hotswap
wireless_hotswap = keyboards_df[(keyboards_df['isWireless'] == 'true') & 
                               (keyboards_df['isHotSwappable'] == 'true')]
```

## Contributing

Contributions to improve this dataset are welcome! If you notice:
- Missing keyboards
- Incorrect specifications
- Outdated information
- Missing images or links

Please submit a pull request or open an issue with your suggested changes.

## License

This dataset is available under the [GNU General Public License v3.0 (GPL-3.0)](https://www.gnu.org/licenses/gpl-3.0.en.html). This is a copyleft license that requires anyone who distributes this code or a derivative work to make the source available under the same terms. This is appropriate for a dataset that can be improved through community contributions and should remain freely available.

Key provisions of GPL-3.0:
- You are free to use, modify, and distribute this dataset
- Any modified versions must also be open source under GPL-3.0
- The complete source must be made available when distributing the work
- Changes must be documented

## Acknowledgements

This dataset builds upon the work of many keyboard enthusiasts, designers, and community members who have documented and shared information about their creations with the mechanical keyboard community.

Special thanks to:
- The [awesome-split-keyboards](https://github.com/diimdeep/awesome-split-keyboards) repository maintainers
- [QMK Firmware](https://qmk.fm/) contributors
- [ZMK Firmware](https://zmk.dev/) contributors
- The split keyboard community across Discord, Reddit, and GeekHack
