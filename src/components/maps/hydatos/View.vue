<template>
    <Viewer
        :imageSource="imageSource"
        :jsonData="jsonData"
        :pFilters="filters"
        :mapName="mapName"
        :gridSizeInPixels="50"
        :coordinatesOffset="1"
        :maximumZoom="150"
    ></Viewer>
</template>

<script>
    import Viewer from '@/components/Viewer/Viewer'

    export default {
        name: 'view-hydatos',
        components: {
            Viewer
        },
        data() {
            return {
                mapName: 'hydatos',
                gridSizeInPixels: 50,
                coordinatesOffset: 1,
                maximumZoom: 150,
                imageSource: require('@/assets/images/maps/hydatos.jpg'),
                jsonData: require('@/assets/zoneJson/hydatos.json'),
                filters: require('@/assets/filters/eureka.json')
            }
        }
    }
</script>
