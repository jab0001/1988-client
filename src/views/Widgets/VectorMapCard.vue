<template>
    <div class="card widget-calendar">
        <div class="card-header">
            <div class="row align-items-center">
                <div class="col-8">
                    <!-- Title -->
                    <h5 class="h3 mb-0">Статистика</h5>
                </div>
                <!-- <div class="col-4 text-right">
                    <a href="#!" class="btn btn-sm btn-neutral">Action</a>
                </div> -->
            </div>
        </div>

      <div class="card-body">
        <world-map class="vector-map vector-map-sm"
                         :map-data="mapData"
                         :points="points">
        </world-map>

        <ul class="list-group list-group-flush list my--3">
          <li class="list-group-item px-0">
            <div class="row align-items-center">
              <div class="col-auto">
                <!-- Country flag -->
                <img src="/img/icons/flags/US.png" alt="Country flag">
              </div>
              <div class="col">
                <small>Страна:</small>
                <h5 class="mb-0">США</h5>
              </div>
              <div class="col">
                <small>Покупки</small>
                <h5 class="mb-0">2500</h5>
              </div>
              <div class="col">
                <small>Прирост</small>
                <h5 class="mb-0">30%</h5>
              </div>
            </div>
          </li>
          <li class="list-group-item px-0">
            <div class="row align-items-center">
              <div class="col-auto">
                <!-- Country flag -->
                <img src="/img/icons/flags/DE.png" alt="Country flag">
              </div>
              <div class="col">
                <small>Страна:</small>
                <h5 class="mb-0">Германия</h5>
              </div>
              <div class="col">
                <small>Покупки:</small>
                <h5 class="mb-0">2500</h5>
              </div>
              <div class="col">
                <small>BПрирост</small>
                <h5 class="mb-0">30%</h5>
              </div>
            </div>
          </li>
          <li class="list-group-item px-0">
            <div class="row align-items-center">
              <div class="col-auto">
                <!-- Country flag -->
                <img src="/img/icons/flags/GB.png" alt="Country flag">
              </div>
              <div class="col">
                <small>Страна:</small>
                <h5 class="mb-0">Великобритания</h5>
              </div>
              <div class="col">
                <small>Покупки:</small>
                <h5 class="mb-0">2500</h5>
              </div>
              <div class="col">
                <small>Прирост</small>
                <h5 class="mb-0">30%</h5>
              </div>
            </div>
          </li>
        </ul>

      </div>

    </div>
</template>
<script>
  import WorldMap from '@/components/WorldMap/WorldMap.vue';
  export default {
    name: 'map-card',
    components: {
      WorldMap
    },
    data() {
      return {
        mapData: {
          AUS: 760,
          BRA: 900,
          CAN: 120,
          DEU: 1300,
          FRA: 540,
          GBR: 690,
          GEO: 200,
          IND: 200,
          ROU: 600,
          RUS: 757,
          USA: 1800
        },
        points: [
          {
            name: 'Brazil',
            centered: 'BRA',
          },
          {
            name: 'France',
            centered: 'FRA',
          },
          {
            name: 'Italy',
            centered: 'ITA',
          },
          {
            name: 'Oman',
            centered: 'OMN',
          },
          {
            name: 'Indonesia',
            centered: 'IDN',
          },
          {
            name: 'Romania',
            centered: 'ROU',
          }
        ]
      }
    }
  }
</script>
