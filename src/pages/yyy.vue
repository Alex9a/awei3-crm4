<template>
  <div>
    <config-table
      name="基础表格"
      :visible="false"
      :pagination="configTablePagination"
      :is-operation="false"
      operation-name="操作"
      :table-data="configTableTabledata"
      :table-data-static="configTableTabledatastatic"
      :table-config="configTableTableconfig"
      :parameter-list="configTableParameterlist"
      url="/deepexi-domain-member/domain/sdk/expirePoints"
      method="POST"
      :query="configTableQuery"
      :body="configTableBody"
      :headers="configTableHeaders"
      table-data-handler="function handleData(response) {
  // 重要：！！返回表格数据 Array 类型
  // return response.payload.content;
  return response.data;
}"
      app-key="qGvwvm29"
      app-secret="30d8302275f788ad2bbe8a94976ddbe1e60d53b7"
      handler-function="function handleData(response) {
  // 重要：！！返回表格数据 Array 类型
  // return response.payload.content;
  return response.data;
}"
      v-roles="''"
    ></config-table>
    <el-data-table
      app-key="qGvwvm29"
      app-secret="30d8302275f788ad2bbe8a94976ddbe1e60d53b7"
      :columns="elDataTableColumns"
      :form="elDataTableForm"
      :form-attrs="elDataTableFormattrs"
      :search-form="elDataTableSearchform"
      :can-search-collapse="true"
      :single="true"
      :has-operation="true"
      :extra-buttons="elDataTableExtrabuttons"
      :header-buttons="elDataTableHeaderbuttons"
      :has-new="true"
      :has-edit="true"
      :has-view="false"
      :has-delete="true"
      new-text="新增"
      edit-text="修改"
      view-text="查看"
      :has-pagination="true"
      :dialog-attrs="elDataTableDialogattrs"
      v-roles="''"
    ></el-data-table>
    <form-container
      :inline="true"
      position="left"
      primary-text="提交"
      :have-second="true"
      second-text="重置"
      v-roles="''"
    >
      <form-input
        :in-container="true"
        type="text"
        placeholder="请输入"
        label="单行文本"
        :is-label-visible="true"
        :status="0"
        :min="2"
        :max="30"
        :require="false"
        :is-show-min="false"
        :is-show-max="false"
        :is-show-customer="false"
        :rules="formInputRules"
        v-roles="''"
      ></form-input>
      <form-input
        type="text"
        placeholder="请输入"
        label="单行文本"
        :is-label-visible="true"
        :status="0"
        :min="2"
        :max="30"
        :require="false"
        :is-show-min="false"
        :is-show-max="false"
        :is-show-customer="false"
        :rules="formInputRules_1"
        v-roles="''"
      ></form-input>
      <form-input
        :in-container="true"
        type="number"
        placeholder="请输入"
        label="数字框"
        :is-label-visible="true"
        :status="0"
        :step="1"
        :min="2"
        :max="30"
        :require="false"
        :is-show-min="false"
        :is-show-max="false"
        :is-show-customer="false"
        :rules="formInputRules_2"
        v-roles="''"
      ></form-input>
      <form-input
        type="text"
        placeholder="请输入"
        label="单行文本"
        :is-label-visible="true"
        :status="0"
        :min="2"
        :max="30"
        :require="false"
        :is-show-min="false"
        :is-show-max="false"
        :is-show-customer="false"
        :rules="formInputRules_3"
        v-roles="''"
      ></form-input>
      <submit-item
        :inline="true"
        position="left"
        primary-text="提交"
        :have-second="true"
        second-text="重置"
        :query="submitItemQuery"
        :body="submitItemBody"
        :headers="submitItemHeaders"
        v-roles="''"
      ></submit-item>
    </form-container>
  </div>
</template>
<script>
export default {
  components: {},
  data: function() {
    return {
      pageName: "工作台",
      configTablePagination: [10],
      configTableTabledata: [],
      configTableTabledatastatic: [
        {
          index: 1,
          creatAt: "2020-04-13 20:25:51",
          updateAt: "2020-04-13 20:26:01",
          createBy: "管理员1"
        },
        {
          index: 2,
          creatAt: "2020-04-13 20:25:51",
          updateAt: "2020-04-13 20:26:01",
          createBy: "管理员2"
        }
      ],
      configTableTableconfig: [
        {
          label: "序号",
          name: "index"
        },
        {
          label: "创建时间",
          name: "creatAt"
        },
        {
          label: "修改时间",
          name: "updateAt"
        },
        {
          label: "创建人",
          name: "createBy"
        }
      ],
      configTableParameterlist: [],
      configTableQuery: {},
      configTableBody: {
        "8": ""
      },
      configTableHeaders: {},
      elDataTableColumns: [
        {
          prop: "index",
          label: "序号"
        },
        {
          prop: "crateAt",
          label: "创建时间"
        },
        {
          prop: "updateAt",
          label: "修改时间"
        },
        {
          prop: "createBy",
          label: "创建人"
        }
      ],
      elDataTableForm: [
        {
          type: "input",
          id: "name",
          label: "单行文本",
          rules: [
            {
              required: true,
              message: "请输入单行文本",
              trigger: "blur"
            }
          ],
          el: {
            placeholder: "请输入单行文本"
          }
        }
      ],
      elDataTableFormattrs: {},
      elDataTableSearchform: [
        {
          el: {
            placeholder: "请输入"
          },
          label: "创建人",
          id: "createBy",
          type: "input"
        }
      ],
      elDataTableExtrabuttons: [
        {
          text: "查看"
        },
        {
          text: "编辑"
        },
        {
          text: "删除"
        }
      ],
      elDataTableHeaderbuttons: [
        {
          text: "新增"
        },
        {
          text: "自定义"
        }
      ],
      elDataTableDialogattrs: {
        "modal-append-to-body": false
      },
      formInputRules: [
        {
          required: false,
          message: "",
          trigger: []
        }
      ],
      formInputRules_1: [
        {
          required: false,
          message: "",
          trigger: []
        }
      ],
      formInputRules_2: [
        {
          required: false,
          message: "",
          trigger: []
        }
      ],
      formInputRules_3: [
        {
          required: false,
          message: "",
          trigger: []
        }
      ],
      submitItemQuery: {},
      submitItemBody: {},
      submitItemHeaders: {}
    }
  },
  mounted: function() {},
  watch: {},
  methods: {},
  destroyed: function() {}
}
</script>
<style lang="less" scoped="scoped"></style>
