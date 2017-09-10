ChartAccent PowerBI Visuals
====

Follow these steps to build the visuals:

1. Make sure you clone the github repos in the following structure:
   - ChartAccent
     - `chartaccent`: https://github.com/chartaccent/chartaccent.git
     - `chartaccent-powerbi`: https://github.com/chartaccent/chartaccent-powerbi.git

2. Build the `chartaccent` repo in its directory

3. Install the PowerBI visual tools: `npm install -g powerbi-visuals-tools`

4. Build all the three visuals: `./make.sh`
    - Each visual has its own `pbiviz.[visual-name].json` (e.g., `pbiviz.barchart.json`)
    - Copy the corresponding `pbiviz.[visual-name].json` to `pbiviz.json`
    - `pbiviz update`
    - `pbiviz package`
    - You can also use `pbiviz start` to serve the visual for debugging. However, you have to restart this command when you update the `chartaccent` repo's code, because the `pbiviz`'s process doesn't detect changes there