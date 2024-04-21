<template>
  <div class="conteiner_main">


    <div class="conteiner_second">


      <div class="list_main">
        <label class="check_mark_label"><input type="checkbox" class="check_mark"
            v-model="string_checked_1"><span></span></label>
        <label class="checkbox_label"><input type="checkbox" class="checkbox_2" v-model="list_checked_1"
            @change="check_all_list_1"><span></span>List 1</label>
      </div>
      <div v-if="string_checked_1">
        <div class="list_seen" v-for="(item, index) in checked_list(4)" :key="index">
          <label>
            <div><input type="checkbox" v-model="item.checked[0]" @change="check_item_1(item)"><span>{{ item.text
                }}</span></div>
            <div><input type="text" v-model="item.price[0]" @change="XXX_1(item)"><input type="color"
                v-model="item.color[0]"></div>
          </label>
        </div>
      </div>


      <div class="list_main">
        <label class="check_mark_label"><input type="checkbox" class="check_mark"
            v-model="string_checked_2"><span></span></label>
        <label class="checkbox_label"><input type="checkbox" class="checkbox_2" v-model="list_checked_2"
            @change="check_all_list_2"><span></span>List 2</label>
      </div>
      <div v-if="string_checked_2">
        <div class="list_seen" v-for="(item, index) in checked_list(6)" :key="index">
          <label>
            <div><input type="checkbox" v-model="item.checked[1]" @change="check_item_2(item)"><span>{{ item.text
                }}</span></div>
            <div><input type="text" v-model="item.price[1]" @change="XXX_2(item)"><input type="color"
                v-model="item.color[1]"></div>
          </label>
        </div>
      </div>


      <div class="list_main">
        <label class="check_mark_label"><input type="checkbox" class="check_mark"
            v-model="string_checked_3"><span></span></label>
        <label class="checkbox_label"><input type="checkbox" class="checkbox_2" v-model="list_checked_3"
            @change="check_all_list_3"><span></span>List 3</label>
      </div>
      <div v-if="string_checked_3">
        <div class="list_seen" v-for="(item, index) in checked_list(5)" :key="index">
          <label>
            <div><input type="checkbox" v-model="item.checked[2]" @change="check_item_3(item)"><span>{{ item.text
                }}</span></div>
            <div><input type="text" v-model="item.price[2]" @change="XXX_3(item)"><input type="color"
                v-model="item.color[2]"></div>
          </label>
        </div>
      </div>


      <div class="list_main">
        <label class="check_mark_label"><input type="checkbox" class="check_mark"
            v-model="string_checked_4"><span></span></label>
        <label class="checkbox_label"><input type="checkbox" class="checkbox_2" v-model="list_checked_4"
            @change="check_all_list_4"><span></span>List 4</label>
      </div>
      <div v-if="string_checked_4">
        <div class="list_seen" v-for="(item, index) in checked_list(6)" :key="index">
          <label>
            <div><input type="checkbox" v-model="item.checked[3]" @change="check_item_4(item)"><span>{{ item.text
                }}</span></div>
            <div><input type="text" v-model="item.price[3]" @change="XXX_4(item)"><input type="color"
                v-model="item.color[3]"></div>
          </label>
        </div>
      </div>


      <div class="list_main">
        <label class="check_mark_label"><input type="checkbox" class="check_mark"
            v-model="string_checked_5"><span></span></label>
        <label class="checkbox_label"><input type="checkbox" class="checkbox_2" v-model="list_checked_5"
            @change="check_all_list_5"><span></span>List 5</label>
      </div>
      <div v-if="string_checked_5">
        <div class="list_seen" v-for="(item, index) in checked_list(4)" :key="index">
          <label class="list_elem">
            <div><input type="checkbox" v-model="item.checked[4]" @change="check_item_5(item)"><span>{{ item.text
                }}</span></div>
            <div><input type="text" v-model="item.price[4]" @change="XXX_5(item)"><input type="color"
                v-model="item.color[4]"></div>
          </label>
        </div>
      </div>

    </div>



    <div class="conteiner_second">



      <div class="conteiner_list">
        <div class="list_head">
          <p>List 1</p>
          <button @click="button_click_1">{{ button_text[0] }}</button>
        </div>


        <div class="list_change" v-if="strong_elem_1">
          <div class="list_element" v-if="items[0].checked[0]">
            <div v-for="index in items[0].price[0]" :key="index">
              <input type="color" v-model="items[0].color[0]">
            </div>
          </div>
          <div class="list_element" v-if="items[1].checked[0]">
            <div v-for="index in items[1].price[0]" :key="index">
              <input type="color" v-model="items[1].color[0]">
            </div>
          </div>
          <div class="list_element" v-if="items[2].checked[0]">
            <div v-for="index in items[2].price[0]" :key="index">
              <input type="color" v-model="items[2].color[0]">
            </div>
          </div>
          <div class="list_element" v-if="items[3].checked[0]">
            <div v-for="index in items[3].price[0]" :key="index">
              <input type="color" v-model="items[3].color[0]">
            </div>
          </div>
        </div>


        <div class="list_element" v-if="mix_elem_1">
          <div v-for="(but, index) in arr_for_rand_1" :key="index">
            <input type="color" v-model="arr_for_rand_1[index]">
          </div>
        </div>
      </div>



      <div class="conteiner_list">

        <div class="list_head">
          <p>List 2</p>
          <button @click="button_click_2">{{ button_text[1] }}</button>
        </div>

        <div class="list_change" v-if="strong_elem_2">
          <div class="list_element" v-if="items[0].checked[1]">
            <div v-for="index in items[0].price[1]" :key="index">
              <input type="color" v-model="items[0].color[1]">
            </div>
          </div>
          <div class="list_element" v-if="items[1].checked[1]">
            <div v-for="index in items[1].price[1]" :key="index">
              <input type="color" v-model="items[1].color[1]">
            </div>
          </div>
          <div class="list_element" v-if="items[2].checked[1]">
            <div v-for="index in items[2].price[1]" :key="index">
              <input type="color" v-model="items[2].color[1]">
            </div>
          </div>
          <div class="list_element" v-if="items[3].checked[1]">
            <div v-for="index in items[3].price[1]" :key="index">
              <input type="color" v-model="items[3].color[1]">
            </div>
          </div>
          <div class="list_element" v-if="items[4].checked[1]">
            <div v-for="index in items[4].price[1]" :key="index">
              <input type="color" v-model="items[4].color[1]">
            </div>
          </div>
          <div class="list_element" v-if="items[5].checked[1]">
            <div v-for="index in items[5].price[1]" :key="index">
              <input type="color" v-model="items[5].color[1]">
            </div>
          </div>

          <div class="list_element" v-if="mix_elem">
            <div v-for="(but, index) in arr_for_rand_1" :key="index">
              <input type="color" v-model="arr_for_rand_1[index]">
            </div>
          </div>

        </div>

        <div class="list_element" v-if="mix_elem_2">
          <div v-for="(but, index) in arr_for_rand_2" :key="index">
            <input type="color" v-model="arr_for_rand_2[index]">
          </div>
        </div>

      </div>



      <div class="conteiner_list">

        <div class="list_head">
          <p>List 3</p>
          <button @click="button_click_3">{{ button_text[2] }}</button>
        </div>

        <div class="list_change" v-if="strong_elem_3">
          <div class="list_element" v-if="items[0].checked[2]">
            <div v-for="index in items[0].price[2]" :key="index">
              <input type="color" v-model="items[0].color[2]">
            </div>
          </div>
          <div class="list_element" v-if="items[1].checked[2]">
            <div v-for="index in items[1].price[2]" :key="index">
              <input type="color" v-model="items[1].color[2]">
            </div>
          </div>
          <div class="list_element" v-if="items[2].checked[2]">
            <div v-for="index in items[2].price[2]" :key="index">
              <input type="color" v-model="items[2].color[2]">
            </div>
          </div>
          <div class="list_element" v-if="items[3].checked[2]">
            <div v-for="index in items[3].price[2]" :key="index">
              <input type="color" v-model="items[3].color[2]">
            </div>
          </div>
          <div class="list_element" v-if="items[4].checked[2]">
            <div v-for="index in items[4].price[2]" :key="index">
              <input type="color" v-model="items[4].color[2]">
            </div>
          </div>
        </div>

        <div class="list_element" v-if="mix_elem_3">
          <div v-for="(but, index) in arr_for_rand_3" :key="index">
            <input type="color" v-model="arr_for_rand_3[index]">
          </div>
        </div>

      </div>



      <div class="conteiner_list">

        <div class="list_head">
          <p>List 4</p>
          <button @click="button_click_4">{{ button_text[3] }}</button>
        </div>

        <div class="list_change" v-if="strong_elem_4">
          <div class="list_element" v-if="items[0].checked[3]">
            <div v-for="index in items[0].price[3]" :key="index">
              <input type="color" v-model="items[0].color[3]">
            </div>
          </div>
          <div class="list_element" v-if="items[1].checked[3]">
            <div v-for="index in items[1].price[3]" :key="index">
              <input type="color" v-model="items[1].color[3]">
            </div>
          </div>
          <div class="list_element" v-if="items[2].checked[3]">
            <div v-for="index in items[2].price[3]" :key="index">
              <input type="color" v-model="items[2].color[3]">
            </div>
          </div>
          <div class="list_element" v-if="items[3].checked[3]">
            <div v-for="index in items[3].price[3]" :key="index">
              <input type="color" v-model="items[3].color[3]">
            </div>
          </div>
          <div class="list_element" v-if="items[4].checked[3]">
            <div v-for="index in items[4].price[3]" :key="index">
              <input type="color" v-model="items[4].color[3]">
            </div>
          </div>
          <div class="list_element" v-if="items[5].checked[3]">
            <div v-for="index in items[5].price[3]" :key="index">
              <input type="color" v-model="items[5].color[3]">
            </div>
          </div>
        </div>

        <div class="list_element" v-if="mix_elem_4">
          <div v-for="(but, index) in arr_for_rand_4" :key="index">
            <input type="color" v-model="arr_for_rand_4[index]">
          </div>
        </div>

      </div>



      <div class="conteiner_list">

        <div class="list_head">
          <p>List 5</p>
          <button @click="button_click_5">{{ button_text[4] }}</button>
        </div>

        <div class="list_change" v-if="strong_elem_5">
          <div class="list_element" v-if="items[0].checked[4]">
            <div v-for="index in items[0].price[4]" :key="index">
              <input type="color" v-model="items[0].color[4]">
            </div>
          </div>
          <div class="list_element" v-if="items[1].checked[4]">
            <div v-for="index in items[1].price[4]" :key="index">
              <input type="color" v-model="items[1].color[4]">
            </div>
          </div>
          <div class="list_element" v-if="items[2].checked[4]">
            <div v-for="index in items[2].price[4]" :key="index">
              <input type="color" v-model="items[2].color[4]">
            </div>
          </div>
          <div class="list_element" v-if="items[3].checked[4]">
            <div v-for="index in items[3].price[4]" :key="index">
              <input type="color" v-model="items[3].color[4]">
            </div>
          </div>
        </div>

        <div class="list_element" v-if="mix_elem_5">
          <div v-for="(but, index) in arr_for_rand_5" :key="index">
            <input type="color" v-model="arr_for_rand_5[index]">
          </div>
        </div>

      </div>



    </div>
  </div>

</template>

<script>
export default {
  name: 'App',
  data() {
    return {
      items: [
        {
          checked: [false, false, false, false, false],
          index: 0,
          text: "Item 1",
          color: ['#ff0000', '#ff0000', '#ff0000', '#ff0000', '#ff0000'],
          price: [0, 0, 0, 0, 0]
        },
        {
          checked: [false, false, false, false, false],
          index: 1,
          text: "Item 2",
          color: ['#8000FF', '#8000FF', '#8000FF', '#8000FF', '#8000FF'],
          price: [0, 0, 0, 0, 0]
        },
        {
          checked: [false, false, false, false, false],
          index: 2,
          text: "Item 3",
          color: ['#FF8000', '#FF8000', '#FF8000', '#FF8000', '#FF8000'],
          price: [0, 0, 0, 0, 0]
        },
        {
          checked: [false, false, false, false, false],
          index: 3,
          text: "Item 4",
          color: ['#808000', '#808000', '#808000', '#808000', '#808000'],
          price: [0, 0, 0, 0, 0]
        },
        {
          checked: [false, false, false, false, false],
          index: 4,
          text: "Item 5",
          color: ['#ffff00', '#ffff00', '#ffff00', '#ffff00', '#ffff00'],
          price: [0, 0, 0, 0, 0]
        },
        {
          checked: [false, false, false, false, false],
          index: 5,
          text: "Item 6",
          color: ['#FFC0CB', '#FFC0CB', '#FFC0CB', '#FFC0CB', '#FFC0CB'],
          price: [0, 0, 0, 0, 0]
        },
      ],
      string_checked_1: false,
      string_checked_2: false,
      string_checked_3: false,
      string_checked_4: false,
      string_checked_5: false,
      list_checked_1: false,
      list_checked_1_sum: 0,
      list_checked_2: false,
      list_checked_2_sum: 0,
      list_checked_3: false,
      list_checked_3_sum: 0,
      list_checked_4: false,
      list_checked_4_sum: 0,
      list_checked_5: false,
      list_checked_5_sum: 0,
      button_text: ['Перемешать','Перемешать','Перемешать','Перемешать','Перемешать'],
      arr_for_rand_1: [],
      arr_for_rand_2: [],
      arr_for_rand_3: [],
      arr_for_rand_4: [],
      arr_for_rand_5: [],
      strong_elem_1: true,
      strong_elem_2: true,
      strong_elem_3: true,
      strong_elem_4: true,
      strong_elem_5: true,
      mix_elem_1: false,
      mix_elem_2: false,
      mix_elem_3: false,
      mix_elem_4: false,
      mix_elem_5: false,
    }
  },
  methods: {
    checked_list(rrr) {
      return this.items.slice(0, rrr);
    },
    check_all_list_1() {
      this.items.forEach(item => {
        item.checked[0] = this.list_checked_1;
        if (this.list_checked_1 === true) {
          item.price[0] = 5;
        } else {
          item.price[0] = 0;
        }
      })
      if (this.list_checked_1 === true) {
        this.list_checked_1_sum = 4;
      } else {
        this.list_checked_1_sum = 0;
      }
      if (this.string_checked_1 === false) {
        this.string_checked_1 = true;
      }
    },
    check_all_list_2() {
      this.items.forEach(item => {
        item.checked[1] = this.list_checked_2;
        if (this.list_checked_2 === true) {
          item.price[1] = 5;
        } else {
          item.price[1] = 0;
        }
      })
      if (this.list_checked_2 === true) {
        this.list_checked_2_sum = 6;
      } else {
        this.list_checked_2_sum = 0;
      }
      if (this.string_checked_2 === false) {
        this.string_checked_2 = true;
      }
    },
    check_all_list_3() {
      this.items.forEach(item => {
        item.checked[2] = this.list_checked_3;
        if (this.list_checked_3 === true) {
          item.price[2] = 5;
        } else {
          item.price[2] = 0;
        }
      })
      if (this.list_checked_3 === true) {
        this.list_checked_3_sum = 5;
      } else {
        this.list_checked_3_sum = 0;
      }
      if (this.string_checked_3 === false) {
        this.string_checked_3 = true;
      }
    },
    check_all_list_4() {
      this.items.forEach(item => {
        item.checked[3] = this.list_checked_4;
        if (this.list_checked_4 === true) {
          item.price[3] = 5;
        } else {
          item.price[3] = 0;
        }
      })
      if (this.list_checked_4 === true) {
        this.list_checked_4_sum = 6;
      } else {
        this.list_checked_4_sum = 0;
      }
      if (this.string_checked_4 === false) {
        this.string_checked_4 = true;
      }
    },
    check_all_list_5() {
      this.items.forEach(item => {
        item.checked[4] = this.list_checked_5;
        if (this.list_checked_5 === true) {
          item.price[4] = 5;
        } else {
          item.price[4] = 0;
        }
      })
      if (this.list_checked_5 === true) {
        this.list_checked_5_sum = 4;
      } else {
        this.list_checked_5_sum = 0;
      }
      if (this.string_checked_5 === false) {
        this.string_checked_5 = true;
      }
    },
    check_item_1(item) {
      if (item.checked[0] === false) {
        item.price[0] = 0;
        this.list_checked_1_sum -= 1;
      } else {
        item.price[0] = 5;
        this.list_checked_1_sum += 1;
        this.list_checked_1 = true;
      }
      if (this.list_checked_1_sum === 0) {
        this.list_checked_1 = false;
      }
    },
    check_item_2(item) {
      if (item.checked[1] === false) {
        item.price[1] = 0;
        this.list_checked_2_sum -= 1;
      } else {
        item.price[1] = 5;
        this.list_checked_2_sum += 1;
        this.list_checked_2 = true;
      }
      if (this.list_checked_2_sum === 0) {
        this.list_checked_2 = false;
      }
    },
    check_item_3(item) {
      if (item.checked[2] === false) {
        item.price[2] = 0;
        this.list_checked_3_sum -= 1;
      } else {
        item.price[2] = 5;
        this.list_checked_3_sum += 1;
        this.list_checked_3 = true;
      }
      if (this.list_checked_3_sum === 0) {
        this.list_checked_3 = false;
      }
    },
    check_item_4(item) {
      if (item.checked[3] === false) {
        item.price[3] = 0;
        this.list_checked_4_sum -= 1;
      } else {
        item.price[3] = 5;
        this.list_checked_4_sum += 1;
        this.list_checked_4 = true;
      }
      if (this.list_checked_4_sum === 0) {
        this.list_checked_4 = false;
      }
    },
    check_item_5(item) {
      if (item.checked[4] === false) {
        item.price[4] = 0;
        this.list_checked_5_sum -= 1;
      } else {
        item.price[4] = 5;
        this.list_checked_5_sum += 1;
        this.list_checked_5 = true;
      }
      if (this.list_checked_5_sum === 0) {
        this.list_checked_5 = false;
      }
    },
    XXX_1(item) {
      item.price[0] = parseInt(item.price[0]);
    },
    XXX_2(item) {
      item.price[1] = parseInt(item.price[1]);
    },
    XXX_3(item) {
      item.price[2] = parseInt(item.price[2]);
    },
    XXX_4(item) {
      item.price[3] = parseInt(item.price[3]);
    },
    XXX_5(item) {
      item.price[4] = parseInt(item.price[4]);
    },
    button_click_1() {
      this.arr_for_rand_1 = [];
      for (let i = 0; i < parseInt(this.items[0].price[0]); i++) {
        this.arr_for_rand_1.push(this.items[0].color[0]);
      }
      for (let i = 0; i < parseInt(this.items[1].price[0]); i++) {
        this.arr_for_rand_1.push(this.items[1].color[0]);
      }
      for (let i = 0; i < parseInt(this.items[2].price[0]); i++) {
        this.arr_for_rand_1.push(this.items[2].color[0]);
      }
      for (let i = 0; i < parseInt(this.items[3].price[0]); i++) {
        this.arr_for_rand_1.push(this.items[3].color[0]);
      }
      let shuffled = [...this.arr_for_rand_1];
      for (let i = shuffled.length - 1; i > 0; i--) {
        const j = Math.floor(Math.random() * (i + 1));
        [shuffled[i], shuffled[j]] = [shuffled[j], shuffled[i]];
      }
      if (this.strong_elem_1 === true) {
        this.strong_elem_1 = false;
        this.mix_elem_1 = true;
      } else {
        this.strong_elem_1 = true;
        this.mix_elem_1 = false;
      }

      this.arr_for_rand_1 = shuffled;
      if (this.button_text[0] === 'Перемешать'){
      this.button_text[0] = 'Сортировать';
      } else {
        this.button_text[0] = 'Перемешать';
      }
    },
    button_click_2() {
      this.arr_for_rand_2 = [];
      for (let i = 0; i < parseInt(this.items[0].price[1]); i++) {
        this.arr_for_rand_2.push(this.items[0].color[1]);
      }
      for (let i = 0; i < parseInt(this.items[1].price[1]); i++) {
        this.arr_for_rand_2.push(this.items[1].color[1]);
      }
      for (let i = 0; i < parseInt(this.items[2].price[1]); i++) {
        this.arr_for_rand_2.push(this.items[2].color[1]);
      }
      for (let i = 0; i < parseInt(this.items[3].price[1]); i++) {
        this.arr_for_rand_2.push(this.items[3].color[1]);
      }
      for (let i = 0; i < parseInt(this.items[4].price[1]); i++) {
        this.arr_for_rand_2.push(this.items[4].color[1]);
      }
      for (let i = 0; i < parseInt(this.items[5].price[1]); i++) {
        this.arr_for_rand_2.push(this.items[5].color[1]);
      }
      let shuffled = [...this.arr_for_rand_2];
      for (let i = shuffled.length - 1; i > 0; i--) {
        const j = Math.floor(Math.random() * (i + 1));
        [shuffled[i], shuffled[j]] = [shuffled[j], shuffled[i]];
      }
      if (this.strong_elem_2 === true) {
        this.strong_elem_2 = false;
        this.mix_elem_2 = true;
      } else {
        this.strong_elem_2 = true;
        this.mix_elem_2 = false;
      }

      this.arr_for_rand_2 = shuffled;
      if (this.button_text[1] === 'Перемешать'){
      this.button_text[1] = 'Сортировать';
      } else {
        this.button_text[1] = 'Перемешать';
      }
    },
    button_click_3() {
      
      this.arr_for_rand_3 = [];
      for (let i = 0; i < parseInt(this.items[0].price[2]); i++) {
        this.arr_for_rand_3.push(this.items[0].color[2]);
      }
      for (let i = 0; i < parseInt(this.items[1].price[2]); i++) {
        this.arr_for_rand_3.push(this.items[1].color[2]);
      }
      for (let i = 0; i < parseInt(this.items[2].price[2]); i++) {
        this.arr_for_rand_3.push(this.items[2].color[2]);
      }
      for (let i = 0; i < parseInt(this.items[3].price[2]); i++) {
        this.arr_for_rand_3.push(this.items[3].color[2]);
      }
      for (let i = 0; i < parseInt(this.items[4].price[2]); i++) {
        this.arr_for_rand_3.push(this.items[4].color[2]);
      }
      let shuffled = [...this.arr_for_rand_3];
      for (let i = shuffled.length - 1; i > 0; i--) {
        const j = Math.floor(Math.random() * (i + 1));
        [shuffled[i], shuffled[j]] = [shuffled[j], shuffled[i]];
      }
      if (this.strong_elem_3 === true) {
        this.strong_elem_3 = false;
        this.mix_elem_3 = true;
      } else {
        this.strong_elem_3 = true;
        this.mix_elem_3 = false;
      }

      this.arr_for_rand_3 = shuffled;
      if (this.button_text[2] === 'Перемешать'){
      this.button_text[2] = 'Сортировать';
      } else {
        this.button_text[2] = 'Перемешать';
      }
    },
    button_click_4() {
      this.arr_for_rand_4 = [];
      for (let i = 0; i < parseInt(this.items[0].price[3]); i++) {
        this.arr_for_rand_4.push(this.items[0].color[3]);
      }
      for (let i = 0; i < parseInt(this.items[1].price[3]); i++) {
        this.arr_for_rand_4.push(this.items[1].color[3]);
      }
      for (let i = 0; i < parseInt(this.items[2].price[3]); i++) {
        this.arr_for_rand_4.push(this.items[2].color[3]);
      }
      for (let i = 0; i < parseInt(this.items[3].price[3]); i++) {
        this.arr_for_rand_4.push(this.items[3].color[3]);
      }
      for (let i = 0; i < parseInt(this.items[4].price[3]); i++) {
        this.arr_for_rand_4.push(this.items[4].color[3]);
      }
      for (let i = 0; i < parseInt(this.items[5].price[3]); i++) {
        this.arr_for_rand_4.push(this.items[5].color[3]);
      }
      let shuffled = [...this.arr_for_rand_4];
      for (let i = shuffled.length - 1; i > 0; i--) {
        const j = Math.floor(Math.random() * (i + 1));
        [shuffled[i], shuffled[j]] = [shuffled[j], shuffled[i]];
      }
      if (this.strong_elem_4 === true) {
        this.strong_elem_4 = false;
        this.mix_elem_4 = true;
      } else {
        this.strong_elem_4 = true;
        this.mix_elem_4 = false;
      }
      this.arr_for_rand_4 = shuffled;
      if (this.button_text[3] === 'Перемешать'){
      this.button_text[3] = 'Сортировать';
      } else {
        this.button_text[3] = 'Перемешать';
      }
    },
    button_click_5() {
      this.arr_for_rand_5 = [];
      for (let i = 0; i < parseInt(this.items[0].price[4]); i++) {
        this.arr_for_rand_5.push(this.items[0].color[4]);
      }
      for (let i = 0; i < parseInt(this.items[1].price[4]); i++) {
        this.arr_for_rand_5.push(this.items[1].color[4]);
      }
      for (let i = 0; i < parseInt(this.items[2].price[4]); i++) {
        this.arr_for_rand_5.push(this.items[2].color[4]);
      }
      for (let i = 0; i < parseInt(this.items[3].price[4]); i++) {
        this.arr_for_rand_5.push(this.items[3].color[4]);
      }
      let shuffled = [...this.arr_for_rand_5];
      for (let i = shuffled.length - 1; i > 0; i--) {
        const j = Math.floor(Math.random() * (i + 1));
        [shuffled[i], shuffled[j]] = [shuffled[j], shuffled[i]];
      }
      if (this.strong_elem_5 === true) {
        this.strong_elem_5 = false;
        this.mix_elem_5 = true;
      } else {
        this.strong_elem_5 = true;
        this.mix_elem_5 = false;
      }

      this.arr_for_rand_5 = shuffled;
      if (this.button_text[4] === 'Перемешать'){
      this.button_text[4] = 'Сортировать';
      } else {
        this.button_text[4] = 'Перемешать';
      }
    },
  }
}



</script>

<style>
/* .list_elem {
  display: flex;
flex-direction: row;
align-items: center;
} */
.list_head {
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  padding: 10px;
}

.list_element {
  display: flex;
  flex-wrap: wrap;

}

.list_change {
  display: flex;
  flex-direction: column;
  width: 100%;
}

input[type="color"] {
  border: none;
  outline: none;
  padding: 0;
  margin: 0;
  width: 25px;
  height: 25px;
}

.conteiner_list {
  border: medium solid black;
  border-radius: 5px;
  margin: 10px;
}

.list_seen label div * {
  margin-top: 2px;
  margin-left: 5px;
}

.list_seen label div {
  display: flex;
}

input[type="text"] {
  width: 23px;

}

.list_seen label {
  width: 60%;
  display: flex;
  flex-direction: row;
  justify-content: space-between;

}

.list_seen {
  display: flex;
  flex-direction: column;
  align-items: center;

}

.list_main {
  padding: 10px;
  display: flex;
}

.list_main .checkbox_2,
.checkbox_label {
  margin-right: 10px;
  margin-left: 10px;
}

.conteiner_main {
  border: medium solid black;
  border-radius: 5px;
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  margin: 50px;
}

.conteiner_second {
  border: medium solid black;
  border-radius: 5px;
  margin: 20px;
  width: 50%;
}

.img_color {
  width: 20px;
  height: 20px;
}

input[type="checkbox"].check_mark {
  display: none;
}

label.check_mark_label {
  width: 15px;
  height: 15px;
  display: block;
  position: relative;
  margin-right: 10px;
  margin-left: 10px;
}

input[type="checkbox"].check_mark+span {
  position: absolute;
  left: 0;
  top: 0;
  width: 100%;
  height: 100%;
  background: url(./images/галка_вправо.png) no-repeat;
  cursor: pointer;
}

input[type="checkbox"].check_mark:checked+span {
  background: url(./images/галка_вниз.png) no-repeat;
}



input[type="checkbox"].checkbox_2 {
  display: none;
}

label.checkbox_label {

  display: flex;
  flex-direction: row;
  justify-content: center;
  align-items: center;

}

input[type="checkbox"].checkbox_2+span {
  width: 15px;
  height: 15px;
  background: url(./images/white_chek.png) no-repeat;
  margin-right: 10px;
  border: medium solid black;
  display: flex;
  flex-direction: row;
  justify-content: center;
  align-items: center;
}

input[type="checkbox"].checkbox_2:checked+span {
  background: url(./images/black_chek.png) no-repeat;
  display: flex;
  flex-direction: row;
  justify-content: center;
  align-items: center;
}
</style>
