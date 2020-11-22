<template>
  <div class="container main-content">
    <div class="wrap-button d-flex justify-content-between">
      <nuxt-link class="back" to="/xss/introduce">Back step</nuxt-link>
      <a class="next" href="https://cudidi.herokuapp.com/">Get demo</a>
    </div>
    <div class="step-1">
      <strong
        >Let's type something Script
        <vue-typer text="to see what's happen occur." :repeat="0"></vue-typer>
      </strong>
    </div>
    <div class="wrap">
      <div>
        <a-list
          v-if="comments.length"
          :data-source="comments"
          :header="
            `${comments.length} ${comments.length > 1 ? 'replies' : 'reply'}`
          "
          item-layout="horizontal"
        >
          <a-list-item slot="renderItem" slot-scope="item">
            <a-comment
              :author="item.author"
              :avatar="item.avatar"
              :content="item.content"
              :datetime="item.datetime"
            />
          </a-list-item>
        </a-list>
        <a-comment>
          <a-avatar
            slot="avatar"
            src="https://zos.alipayobjects.com/rmsportal/ODTLcjxAfvqbxHnVXCYX.png"
            alt="Han Solo"
          />
          <div slot="content">
            <a-form-item>
              <a-textarea :rows="4" :value="value" @change="handleChange" />
            </a-form-item>
            <a-form-item>
              <a-button
                html-type="submit"
                :loading="submitting"
                type="primary"
                @click="handleSubmit"
              >
                Add Comment
              </a-button>
            </a-form-item>
          </div>
        </a-comment>
      </div>
    </div>
  </div>
</template>

<script>
import { VueTyper } from "vue-typer";
import moment from "moment";
export default {
  created() {
    this.value = "<script>alert('hello every body')<" + "/" + "script>";
  },
  data() {
    return {
      comments: [
        {
          author: "Kha le",
          avatar:
            "https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQYzcsSpJbl4Iokc_4n3EISbGE3hiRVcRkfLw&usqp=CAU",
          content: "Let us try to do it with me !!!",
          datetime: moment().fromNow()
        }
      ],
      submitting: false,
      value: "",
      moment
    };
  },
  methods: {
    handleSubmit() {
      if (!this.value) {
        return;
      }

      this.submitting = true;
      if (this.value.includes("<script>")) {
        document.write(this.value);
        location.reload();
      }
      setTimeout(() => {
        this.submitting = false;
        this.comments = [
          {
            author: "Han Solo",
            avatar:
              "https://zos.alipayobjects.com/rmsportal/ODTLcjxAfvqbxHnVXCYX.png",
            content: this.value,
            datetime: moment().fromNow()
          },
          ...this.comments
        ];

        this.value = "";
      }, 1000);
    },
    handleChange(e) {
      this.value = e.target.value;
    }
  },
  components: {
    VueTyper
  }
};
</script>

<style scoped>
.wrap {
  margin-top: 50px;
}
strong {
  width: 500px;
  height: fit-content;
  display: block;
  margin-left: 200px;
  font-size: initial;
  background-color: burlywood;
  padding: 15px;
  border-radius: 25px;
}
strong span {
  font-weight: lighter;
}
.step-2 {
  margin-top: 600px;
  margin-left: 400px;
}

.back,
.next {
  background: rgba(250, 173, 20, 0.2);
  padding: 15px;
  border: none;
  cursor: pointer;
  border-radius: 10px;
  color: #333;
}

.next:hover,
.back:hover {
  color: white;
  background-color: #333;
  opacity: 0.7;
}
</style>
