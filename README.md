# Thanks  
 [CorpGlory](https://github.com/CorpGlory/grafana-graph-panel)


# Screenshots

add crosshair of x-y axis

![Screenshot1](/img/img1.png)

# Graph Panel

Webpack copy of [Grafana default panel](http://docs.grafana.org/features/panels/graph/). 
Now you can make your plugins based on graph panel and hack it easier.

Works only on Grafana versions >= V5.0.1 

# Build

```
npm install
npm run build
```

# After you fork

Sorry, but it's common for Grafana plugins make directives which collide with each other. It comes from AngularJS.
Use `ctrl+f` to find params in source code files below: 

* Change in `plugin.json` id from `graph-panel-og` to `something-else-graph-panel`
* Change in `src/graph.ts` directive name from `grafanaOgGraph` to `somethingElseGraph`
* Change in `src/legend.ts` directive name from `graphOgLegend` to `somethingElseLegend`
* Change in `src/axes_editor` param `templateUrl` param from `public/plugins/graph-panel-og/partials/axes_editor.html` to `public/plugins/something-else-graph-panel/partials/axes_editor.html`
* Change in `template.ts` param `grafana-og-graph` to `something-else-graph` and `graph-og-legend` to `something-else-legend`
* in case you debug with VSCode, change in `.vscode/launch.json` param `/public/plugins/graph-panel-og` to `/public/plugins/something-else-graph-panel`

# Credits

Made by [CorpGlory Dev Team](https://corpglory.com)

Based on 

* [grafana-plugin-template-webpack-typescript](https://github.com/CorpGlory/grafana-plugin-template-webpack-typescript) 
* [@types/grafana](https://github.com/CorpGlory/types-grafana)
