<template>
  <div>
    <v-container>
      <h1 class="headline font-weight-bold">Lists</h1>
      <p class="body-1">v-list 선언을 먼저 하자.</p>
    </v-container>
    <v-container>
      <hr class="contour" />
      <h2 class="title font-weight-bold">Multi Lines</h2>
      <p class="body-1">
        v-list-item에 two-line, three-line props로 몇줄인지 표시할 수 있다.
      </p>
      <div class="code-box">
        <v-list>
          <v-list-item>
            <v-list-item-content>
              <v-list-item-title>Single-line item</v-list-item-title>
            </v-list-item-content>
          </v-list-item>

          <v-list-item two-line>
            <v-list-item-content>
              <v-list-item-title>Two-line item</v-list-item-title>
              <v-list-item-subtitle>Secondary text</v-list-item-subtitle>
            </v-list-item-content>
          </v-list-item>

          <v-list-item three-line>
            <v-list-item-content>
              <v-list-item-title>Three-line item</v-list-item-title>
              <v-list-item-subtitle>
                Secondary line text Lorem ipsum dolor sit amet,
              </v-list-item-subtitle>
              <v-list-item-subtitle>
                consectetur adipiscing elit.
              </v-list-item-subtitle>
            </v-list-item-content>
          </v-list-item>
        </v-list>
      </div>
    </v-container>
    <v-container>
      <hr class="contour" />
      <h2 class="title font-weight-bold">Subheader</h2>
      <p class="body-1">
        Subheader를 통해 리스트에 제목을 달 수 있다.
      </p>
      <div class="code-box">
        <v-list>
          <v-subheader>subheader</v-subheader>
          <v-list-item two-line>
            <v-list-item-content>
              <v-list-item-title>Two-line item</v-list-item-title>
              <v-list-item-subtitle>Secondary text</v-list-item-subtitle>
            </v-list-item-content>
          </v-list-item>

          <v-list-item two-line>
            <v-list-item-content>
              <v-list-item-title>Two-line item</v-list-item-title>
              <v-list-item-subtitle>Secondary text</v-list-item-subtitle>
            </v-list-item-content>
          </v-list-item>
        </v-list>
      </div>
    </v-container>
    <v-container>
      <hr class="contour" />
      <h2 class="title font-weight-bold">Icons and Avatars</h2>
      <p class="body-1">
        v-list-item 이전에 v-list-item-icon, v-list-item-avatar를 사용해서
        리스트 프로필을 만들 수 있다.
      </p>
      <div class="code-box">
        <v-list>
          <v-subheader>subheader</v-subheader>
          <v-list-item two-line>
            <v-list-item-icon>
              <v-icon>mdi-heart</v-icon>
            </v-list-item-icon>
            <v-list-item-content>
              <v-list-item-title>Two-line item</v-list-item-title>
              <v-list-item-subtitle>Secondary text</v-list-item-subtitle>
            </v-list-item-content>
          </v-list-item>

          <v-list-item two-line>
            <v-list-item-avatar color="orange">
              <v-avatar>
                <span class="white--text font-weight-bold">AT</span>
              </v-avatar>
            </v-list-item-avatar>
            <v-list-item-content>
              <v-list-item-title>Two-line item</v-list-item-title>
              <v-list-item-subtitle>Secondary text</v-list-item-subtitle>
            </v-list-item-content>
          </v-list-item>
        </v-list>
      </div>
    </v-container>
    <v-container>
      <hr class="contour" />
      <h2 class="title font-weight-bold">Actions</h2>
      <p class="body-1">
        v-list-item-action 으로 항목 끝에 action button을 넣을 수 있다.
      </p>
      <div class="code-box">
        <v-list>
          <v-subheader>subheader</v-subheader>
          <v-list-item two-line>
            <v-list-item-icon>
              <v-icon>mdi-heart</v-icon>
            </v-list-item-icon>
            <v-list-item-content>
              <v-list-item-title>Two-line item</v-list-item-title>
              <v-list-item-subtitle>Secondary text</v-list-item-subtitle>
            </v-list-item-content>
            <v-list-item-action>
              <v-btn icon>
                <v-icon color="grey lighten-1">mdi-information</v-icon>
              </v-btn>
            </v-list-item-action>
          </v-list-item>

          <v-list-item two-line>
            <v-list-item-avatar color="orange">
              <v-avatar>
                <span class="white--text font-weight-bold">AT</span>
              </v-avatar>
            </v-list-item-avatar>
            <v-list-item-content>
              <v-list-item-title>Two-line item</v-list-item-title>
              <v-list-item-subtitle>Secondary text</v-list-item-subtitle>
            </v-list-item-content>
            <v-list-item-action>
              <v-btn icon>
                <v-icon color="grey lighten-1">mdi-information</v-icon>
              </v-btn>
            </v-list-item-action>
          </v-list-item>
        </v-list>
      </div>
    </v-container>
    <v-container>
      <hr class="contour" />
      <h2 class="title font-weight-bold">Groups</h2>
      <p class="body-1">
        v-list-item-group으로 선택된 값을 저장할 수 있다.<br />
        props active-class로 클래스를 지정할 수 있다.<br />
        props mandatory으로 값을 하나만 선택하는 것을 명시한다.<br />
        props multiple으로 값을 여러개 선택할 수 있다.<br />
        v-list에 props flat를 적용할 수 있으며,<br />
        v-list-item-group에 color를 지정할 수 있다.<br />
        기본 slot으로 active 값을 가져올 수 있다.
      </p>
      <div class="code-box">
        <h4>Selected index or value: {{ group1 }}</h4>
        <v-list>
          <v-subheader>subheader</v-subheader>
          <v-list-item-group
            v-model="group1"
            active-class="red white--text"
            mandatory
          >
            <v-list-item two-line>
              <v-list-item-avatar color="orange">
                <v-avatar>
                  <span class="white--text font-weight-bold">AT</span>
                </v-avatar>
              </v-list-item-avatar>
              <v-list-item-content>
                <v-list-item-title>Two-line item</v-list-item-title>
                <v-list-item-subtitle>Secondary text</v-list-item-subtitle>
              </v-list-item-content>
              <v-list-item-action>
                <v-btn icon>
                  <v-icon color="grey lighten-1">mdi-information</v-icon>
                </v-btn>
              </v-list-item-action>
            </v-list-item>
            <v-list-item two-line value="value">
              <v-list-item-icon>
                <v-icon>mdi-heart</v-icon>
              </v-list-item-icon>
              <v-list-item-content>
                <v-list-item-title>Two-line item</v-list-item-title>
                <v-list-item-subtitle>Secondary text</v-list-item-subtitle>
              </v-list-item-content>
              <v-list-item-action>
                <v-btn icon>
                  <v-icon color="grey lighten-1">mdi-information</v-icon>
                </v-btn>
              </v-list-item-action>
            </v-list-item>
          </v-list-item-group>
        </v-list>
        <h4>Selected index or value: {{ group2 }}</h4>
        <v-list flat>
          <v-subheader>Props multiple and flat</v-subheader>
          <v-list-item-group v-model="group2" multiple color="red">
            <v-list-item two-line>
              <v-list-item-avatar color="orange">
                <v-avatar>
                  <span class="white--text font-weight-bold">AT</span>
                </v-avatar>
              </v-list-item-avatar>
              <v-list-item-content>
                <v-list-item-title>Two-line item</v-list-item-title>
                <v-list-item-subtitle>Secondary text</v-list-item-subtitle>
              </v-list-item-content>
              <v-list-item-action>
                <v-btn icon>
                  <v-icon color="grey lighten-1">mdi-information</v-icon>
                </v-btn>
              </v-list-item-action>
            </v-list-item>
            <v-list-item two-line value="value">
              <v-list-item-icon>
                <v-icon>mdi-heart</v-icon>
              </v-list-item-icon>
              <v-list-item-content>
                <v-list-item-title>Two-line item</v-list-item-title>
                <v-list-item-subtitle>Secondary text</v-list-item-subtitle>
              </v-list-item-content>
              <v-list-item-action>
                <v-btn icon>
                  <v-icon color="grey lighten-1">mdi-information</v-icon>
                </v-btn>
              </v-list-item-action>
            </v-list-item>
          </v-list-item-group>
        </v-list>
        <h4>Selected index or value: {{ group3 }}</h4>
        <v-list flat>
          <v-subheader>Props multiple and flat</v-subheader>
          <v-list-item-group v-model="group3" multiple color="red">
            <v-list-item two-line>
              <template #default="{ active }">
                <v-list-item-avatar color="orange">
                  <v-avatar>
                    <span class="white--text font-weight-bold">AT</span>
                  </v-avatar>
                </v-list-item-avatar>
                <v-list-item-content>
                  <v-list-item-title>
                    Two-line item {{ active }}
                  </v-list-item-title>
                  <v-list-item-subtitle>Secondary text</v-list-item-subtitle>
                </v-list-item-content>
                <v-list-item-action>
                  <v-btn icon>
                    <v-icon color="grey lighten-1">mdi-information</v-icon>
                  </v-btn>
                </v-list-item-action>
              </template>
            </v-list-item>
            <v-list-item two-line value="value">
              <template #default="{ active }">
                <v-list-item-icon>
                  <v-icon>mdi-heart</v-icon>
                </v-list-item-icon>
                <v-list-item-content>
                  <v-list-item-title
                    >Two-line item {{ active }}</v-list-item-title
                  >
                  <v-list-item-subtitle>Secondary text</v-list-item-subtitle>
                </v-list-item-content>
                <v-list-item-action>
                  <v-btn icon>
                    <v-icon color="grey lighten-1">mdi-information</v-icon>
                  </v-btn>
                </v-list-item-action>
              </template>
            </v-list-item>
          </v-list-item-group>
        </v-list>
      </div>
    </v-container>
  </div>
</template>
<script>
export default {
  data() {
    return {
      group1: 0,
      group2: [],
      group3: []
    };
  }
};
</script>
