<template>
  <div class="timeline">
    <div class="timeline-row">
      <div class="timeline-cell" v-for="(item, index) in list" :key="index">{{ item }}</div>
    </div>
    <div class="events">
      <div class="event-container">
        <div class="event-bg"></div>
        <div class="eventRow relative">
          <div class="eventContent">
            <div class="eventItem bg-white">
              <div class="relative">
                <div class="eventBar"></div>
              </div>
            </div>
          </div>
        </div>
        <div class="eventRow relative">
          <div class="eventContent">
            <div class="eventItem">
              <div class="relative">
                <div class="eventBar"></div>
              </div>
            </div>
          </div>
        </div>
        <div class="sticky">
          <button class="projectName">
            <span class="eventText">project 1</span>
            <svg
              xmlns="http://www.w3.org/2000/svg"
              class="arrow"
              viewBox="0 0 20 20"
              fill="currentColor"
            >
              <path
                fill-rule="evenodd"
                d="M14.707 12.707a1 1 0 01-1.414 0L10 9.414l-3.293 3.293a1 1 0 01-1.414-1.414l4-4a1 1 0 011.414 0l4 4a1 1 0 010 1.414z"
                clip-rule="evenodd"
              />
            </svg>
          </button>
        </div>
        <!-- <div class="eventRow"></div> -->
      </div>
    </div>
  </div>
</template>
<script>
export default {
  data() {
    return {
      list: ['meta', 'test/table-name1', 'test/table-name2', 'test/table-name3', 'test/table-name4']
    }
  }
}
</script>
<style lang="stylus" scoped>
.timeline-row {
  width: 100%;
  display: flex;
  align-items: center;
  .timeline-cell {
    width: 200px;
    box-sizing: border-box;
    padding: 0 20px;
    height: 32px;
    background: #ff0;
    display: flex;
    align-items: center;
    justify-content: center;
    border-right: 1px solid #fff;
  }
}
.events {
  .event-container {
    position relative;
    display: flex;
    flex-direction: column;
    .event-bg {
      position absolute;
      height 100%;
      border-radius: 4px;
      background-color rgba(211, 54, 177, 0.05)
      outline rgba(211, 54, 177, 0.12) solid 1px;
      width: max(64px, 200px);
    }
    .eventRow {
      width: 200px;
      border-radius: 5px;
      // height: 10px;
      flex-shrink: 0;
      padding: 0 8px;
    }
    .sticky {
      position: sticky;
      top: 0;
      order: -9999;
      .projectName {
        padding: 2px 8px;
        border-radius: 8px;
        display: flex;
        position: sticky;
        font-size: 14px;
        background-color: rgba(212, 50, 56, 0.25);
      }
    }
  }
}
.eventContent {
  display: flex;
  flex-direction: row;
  .eventItem {
    padding: 6px 8px;
    border-radius: 4px;
    margin: 2px -8px;
    .eventBar {
      width 180px;
      border-radius: 5px;
      height: 10px;
      flex-shrink: 0;
      background-color: rgba(22, 163, 76, 0.8);
    }
  }
}
.arrow {
  width 16px;
  height: 16px;
  margin: 0 auto;
}
.bg-white {
  background-color: #fff;
}
.relative {
  position relative
}
</style>