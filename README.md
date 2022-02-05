# Encapsulating Component Rules

These rules are aimed at standardizing the development of components using React.

## 1. Component directory structure
```
<ComponentName> .................................... 1.1
    <ComponentName>.(jsx|tsx) ...................... 1.2
    <ComponentName>(.module)?.(css|sass|less|styl) . 1.3
    <ComponentName>.d.ts ........................... 1.4
    index.(js|ts) .................................. 1.5
    <ComponentFragmentName>.(jsx|tsx) .............. 1.6
    <ComponentFragmentName>.d.ts ................... 1.4
    README.md ...................................... 1.7
```
### 1.1 Component directory
- PascalCase notation MUST be used in `<ComponentName>`.
- Do NOT USE nested directories. It's keep component structure flat and simple.

### 1.2 Component source (required)
- Component file name MUST be like Component directory name. It's allow identify component as primary.

### 1.3 Component styles (required)
- Style file name MUST be like Component directory name.
- If using CSS Modules, file name MUST be extended with suffix `.module`.
- Allow using CSS preprocessors.

### 1.4 Typing module (required)

### 1.5 Entry point (required)
- MUST export primary component. It's allow use short path in imports of component.
- DO NOT implement component in this file. If you work with different components, it will be difficult to understand where which one is.

``` js
import ComponentName from './ComponentName';
export default ComponentName;
```

### 1.6 Fragments (optional)
Fragment component using in primary component.

### 1.7 Readme (required)
Component documentation 
