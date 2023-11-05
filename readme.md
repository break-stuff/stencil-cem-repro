# Strencil / CEM Analyzer Repro

This repo is to illustrate an issue with generating a custom elements manifest in Stencil components with the CEM Analyzer.

The issue is the analyzer generates an attribute and property for all properties in the component, even if the `@Prop()` is intended to be only a property. There doesn't seem to be a way to differentiate attributes from properties in Stencil.

To repro the issue:

- `npm install`
- `npm run anlyze`

Note that there is an attribute and a property for the `gridData` property in the `custom-elements.json`.