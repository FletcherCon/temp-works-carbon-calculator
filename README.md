# Temporary Works Carbon Calculator

A web-based tool for calculating embodied carbon emissions from temporary works in construction projects, based on the Groundforce Shorco methodology.

## Live Demo

[View the calculator here] (https://fletchercon.github.io/temp-works-carbon-calculator/)

## Overview

This calculator helps construction professionals estimate the carbon footprint of temporary works equipment such as:
- Trench boxes
- Shoring systems
- Scaffolding
- Excavation support
- Hydraulic bracing
- Sheet piles

The tool calculates carbon emissions across two key lifecycle stages:
- **A1-A3**: Embodied carbon from manufacturing
- **A4**: Transport emissions

## Features

- **Easy-to-use interface** - Add multiple equipment items with a simple form
- **Real-time calculations** - Instant carbon footprint updates
- **Visual breakdown** - See embodied vs transport emissions separately
- **CSV Export** - Download results for reporting and record-keeping
- **Accurate methodology** - Based on industry-standard Groundforce Shorco approach
- **Responsive design** - Works on desktop, tablet, and mobile devices

## Getting Started

### Option 1: Use Online
Simply visit the [live calculator](https://fletchercon.github.io/temp-works-carbon-calculator/) and start calculating.

### Option 2: Run Locally
1. Download `index.html` from this repository
2. Open the file in any modern web browser
3. No installation or setup required!

## How to Use

1. **Enter equipment details:**
   - Description (e.g., "Trench Box Type A")
   - Equipment type (Steel or Aluminum)
   - Weight in kilograms
   - Hire duration in weeks
   - Transport distance in kilometers (optional)

2. **Add items** to your project list

3. **Review totals:**
   - Embodied carbon (manufacturing)
   - Transport carbon
   - Total project emissions

4. **Export results** to CSV for documentation

## Methodology

This calculator implements the methodology published by Groundforce Shorco for calculating embodied CO2e in temporary works:

### Carbon Rates (Example Values)
- **Steel**: 2.5 kg CO2e per tonne per week
- **Aluminum**: 8.5 kg CO2e per tonne per week
- **Transport**: 0.062 kg CO2e per tonne per km (round trip)

### Calculation Formula

```
Embodied Carbon = (Weight in tonnes) × (CO2e rate) × (Hire duration in weeks)
Transport Carbon = (Weight in tonnes) × (Distance in km) × 2 × (Transport rate)
Total Carbon = Embodied Carbon + Transport Carbon
```

### Lifecycle Stages
Following BS EN 15978 standards:
- **A1-A3**: Raw material extraction, transport, and manufacturing
- **A4**: Transport to construction site

## ⚠️ Important Notes

- The CO2e rates provided are **example values** for demonstration purposes
- For accurate project calculations, refer to the [Groundforce Shorco technical guide](https://www.vpgroundforce.com/gb/footer-links/useful-links/carbon-calculator-technical-note/)
- Update the rates in the code to match your specific equipment and supplier data
- This tool accounts for equipment reuse through the weekly hire duration methodology

## Customization

To update the carbon rates for your specific equipment:

1. Open `index.html` in a text editor
2. Find the `co2Rates` object in the JavaScript section:
```javascript
const co2Rates = {
    steel: 2.5,      // Update this value
    aluminum: 8.5    // Update this value
};
```
3. Update the `transportRate` value if needed
4. Save and refresh the page

## References

- [Groundforce Shorco Carbon Calculator Technical Note](https://www.vpgroundforce.com/gb/footer-links/useful-links/carbon-calculator-technical-note/)
- [BS EN 15978 - Sustainability of construction works](https://www.en-standard.eu/bs-en-15978-2011-sustainability-of-construction-works-assessment-of-environmental-performance-of-buildings-calculation-method/)
- [VP Group Sustainability Report](https://sustainability.vpplc.com/)

## Contributing

Contributions are welcome! Feel free to:
- Report bugs by opening an issue
- Suggest new features
- Submit pull requests with improvements

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Acknowledgments

- Methodology based on work by Groundforce Shorco
- Built to support sustainable construction practices
- Inspired by the need for accessible carbon accounting tools in the construction industry

## Contact

For questions, suggestions, or feedback, please open an issue on this repository.

---
