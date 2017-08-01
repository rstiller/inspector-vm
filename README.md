# inspector-vm

NodeJS VM Metric Collector

<p align="center">
    <a href="https://www.npmjs.org/package/inspector-vm">
        <img src="https://img.shields.io/npm/v/inspector-vm.svg" alt="NPM Version">
    </a>
    <a href="https://www.npmjs.org/package/inspector-vm">
        <img src="https://img.shields.io/npm/l/inspector-vm.svg" alt="License">
    </a>
    <a href="https://travis-ci.org/rstiller/inspector-vm">
        <img src="http://img.shields.io/travis/rstiller/inspector-vm/master.svg" alt="Build Status">
    </a>
    <a href="https://david-dm.org/rstiller/inspector-vm">
        <img src="https://img.shields.io/david/rstiller/inspector-vm.svg" alt="Dependencies Status">
    </a>
</p>

## install

`npm install --save inspector-vm`

## basic usage

```typescript
import { MetricRegistry } from "inspector-metrics";
import { V8MemoryMetrics } from "inspector-vm";

// get a registry
const registry: MetricRegistry = ...;

// instance the memory metric, contains
//   - space statistics
//   - memory statistics
const memoryMetrics: V8MemoryMetrics = new V8MemoryMetrics("v8", registry.getDefaultClock());

// metric is registered und the name "v8"
// defaults to group "gc"
registry.register(memoryMetrics.getName(), memoryMetrics);

// setup reporter ...
```

## License

[MIT](https://www.opensource.org/licenses/mit-license.php)
