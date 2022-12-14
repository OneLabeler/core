# image data type

Declaration of the image data type display.

## API

### BaseDisplay

The vue component to display a single data object.

#### Props

| Name         | Type              | Description                      |
| ------------ | ----------------- | -------------------------------- |
| `dataObject` | `DataObjectImage` | The data object to be displayed. |

#### Slots

| Name      | Description                                              |
| --------- | -------------------------------------------------------- |
| `overlay` | Use this slot to overlay label tasks' interaction layer. |

## Usage

```vue
<script setup lang="ts">
import { dataTypeImage } from '@onelabeler/core'

const dataObject = {
  uuid: '123',
  value: {
    url: 'https://upload.wikimedia.org/wikipedia/commons/thumb/5/52/Playfair_TimeSeries-2.png/640px-Playfair_TimeSeries-2.png',
    width: 2067,
    height: 1527,
    filename: 'Playfair TimeSeries-2.png',
  },
}
const { BaseDisplay } = dataTypeImage
</script>

<template>
  <div
    style="border-width: 2px; border-style: solid; border-color: black; display: inline-flex"
  >
    <BaseDisplay
      :data-object="dataObject"
      :style="{
        width: `${dataObject.value.width / 4}px`,
        height: `${dataObject.value.height / 4}px`,
      }"
    />
  </div>
</template>
```
