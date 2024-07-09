<template>
  <div class="form-progress-section">
    <ul class="progressbar">
      <li class="active">
        <span class="text">Setup an Account</span>
      </li>
      <li>
        <span class="text">Done!</span>
      </li>
    </ul>
  </div>
</template>

<script>
  export default {}
</script>

<style lang="less" scoped>
.form-progress-section {
  max-width: 1280px;
  width: 100%;
  margin: 24px auto;

  .progressbar {
    list-style-type: none;
    counter-reset: step;
    padding: 0;
    margin: 0 auto;
    
    li {
      float: left;
      width: 50%;
      position: relative;
      text-align: center;
      font-weight: 600;

      &:before {
        content:counter(step);
        counter-increment: step;
        width: 40px;
        height: 40px;
        border: 2px solid @progressInactive;
        display: block;
        margin: 0 auto 10px auto;
        border-radius: 50%;
        line-height: 36px;
        background: @progressInactive;
        color: @progressInactiveText;
        text-align: center;
        font-weight: bold;
      }

      &:after {
        content: '';
        position: absolute;
        width: 160%;
        height: 3px;
        background: @progressPath;
        top: 18px;
        left: -80%;
        z-index: -1;
      }

      &:first-child:before {
        margin-left: 20%;
      }

      &:last-child:before {
        margin-right: 20%;
      }

      &:first-child:after {
        content: none;
      }

      &.active:before {
        border-color: @progressInactive;
        background: @progressActiveBg;
        color: white
      }

      &.active:after {
        background: @progressActiveBg;
      }

      &:first-child {
        text-align: left;
      
        & span.text {
          margin-left: 12%;
        }
      }

      &:last-child {
        text-align: right;
        
        & span.text {
          margin-right: 20%;
        }
      }
    }

    li.active + li:after {
      background: @progressInactive;
    }

    li.active + li:before {
      border-color: @progressInactive;
      background: @progressInactive;
      color: @progressInactiveText
    }
  }
}

@media (max-width: 768px) {
  .form-progress-section {
    .progressbar {
      li {
        &:first-child {
          & span.text {
            margin-left: 8%;
          }
        }
      }
    }
  }
}

@media (max-width: 425px) {
  .form-progress-section {
    .progressbar {
      li {
        &:first-child {
          & span.text {
            margin-left: 0;
          }
        }

        &:last-child {
          & span.text {
            margin-right: 18%;
          }
        }
      }
    }
  }
}
</style>
