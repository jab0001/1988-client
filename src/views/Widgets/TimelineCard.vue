<template>
  <div class="card">
    <!-- Card header -->
    <div class="card-header">
      <!-- Title -->
      <h5 class="h3 mb-0">Latest notifications</h5>
    </div>
    <!-- Card body -->
    <div class="card-body">
      <div class="timeline timeline-one-side" data-timeline-content="axis" data-timeline-axis-style="dashed">
        <div v-for="event in events"
             :key="event.title"
             class="timeline-block">
          <span class="timeline-step" :class="`badge-${event.type}`">
            <i :class="event.icon"></i>
          </span>
          <div class="timeline-content">
            <div class="d-flex justify-content-between pt-1">
              <div>
                <span class="text-muted text-sm font-weight-bold">{{event.title}}</span>
              </div>
              <div class="text-right">
                <small class="text-muted"><i class="fas fa-clock mr-1"></i>{{event.time}}</small>
              </div>
            </div>
            <h6 class="text-sm mt-1 mb-0">{{event.description}}</h6>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
  export default {
    name: 'timeline-card',
    data() {
      return {
        events: [
          {
            title: 'Новое сообщение',
            description: 'Давай встретимся в Старбаксе в 11:30. ',
            icon: 'ni ni-bell-55',
            type: 'success',
            time: '2 часа назад'
          },
          {
            title: 'Новое сообщение',
            description: 'Сообщается о новой проблеме для 1688.',
            icon: 'ni ni-html5',
            type: 'danger',
            time: '3 часа назад'
          },
          {
            title: 'Новое сообщение',
            description: 'Ваши посты очень понравились.',
            icon: 'ni ni-like-2',
            type: 'info',
            time: '5 часов назад'
          }
        ]
      }
    }
  }
</script>
<style>
</style>
