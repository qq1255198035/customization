<template>
      <div id="test">
            <order-list></order-list>
            <goods-list></goods-list>
            <order-item>
                  <div class="hiden-menu">
                        <a-icon type="ellipsis" style="transform: rotate(90deg);font-size: 20px;cursor: pointer" @click="hidemenu = !hidemenu"/>
                        <ul v-show="hidemenu">
                              <li style="border-bottom: 1px solid #fff;">
                                    <a-icon type="search" />查看
                              </li>
                              <li>
                                    <a-icon type="branches" />分享
                              </li>
                        </ul>
                  </div>
            </order-item>
            <a-radio-group>
                  <a-radio-button value="large">Large</a-radio-button>
                  <a-radio-button value="default">Default</a-radio-button>
                  <a-radio-button value="small">Small</a-radio-button>
            </a-radio-group>
            <table-item>
                  <a href="" style="font-size: 14px; text-decoration: underline">查看尺寸表</a>
            </table-item>
            <card-header></card-header>
            <my-title :title="itemTitle">
                  <a-button size="small">返回</a-button>
            </my-title>
            <my-header></my-header>
            <my-stpes :mycurrent="2">
                  <p slot="p1">选择尺码</p>
                  <p slot="p2">确认支付</p>
                  <p slot="p3">等待开团</p>
                  <p slot="p4">完成</p>
            </my-stpes>
            <my-table></my-table>
            <a-input></a-input>
            <a-checkbox>自动登录</a-checkbox>
            <a-date-picker dropdownClassName="my-date-picker"/>
            <a-modal
                  title="管理地址"
                  v-model="show"
                  :footer="null"
            >
                  <p>Bla bla ...</p>
                  <p>Bla bla ...</p>
                  <p>Bla bla ...</p>
            </a-modal>
            
      </div>
</template>
<script>

import MyTable from "@/components/MyTable/MyTable";
import MyStpes from "@/components/MyStpes/MyStpes";
import MyHeader from "@/components/MyHeader/MyHeader";
import MyTitle from "@/components/MyTitle/MyTitle";
import CardHeader from "@/components/CardHeader/CardHeader";
import TableItem  from "@/components/TableItem/TableItem";
import OrderItem  from "@/components/OrderItem/OrderItem";
import GoodsList  from "@/components/GoodsList/GoodsList";
import OrderList  from "@/components/OrderList/OrderList";
export default {
      components:{
            MyTable,
            MyStpes,
            MyHeader,
            MyTitle,
            CardHeader,
            TableItem,
            OrderItem,
            GoodsList,
            OrderList
      },
      data(){
            return{
                  number:0,
                  show: false,
                  itemTitle: '订单详情',
                  hidemenu:false
            }
      },
      methods:{
           
      }
}
</script>
<style lang="less">
#test{
      width: 100%;
      height: 100%;
      padding: 150px 80px;
      background-image: linear-gradient(-45deg, #11bbe8 10%, #4ac37a 100%);
      .hiden-menu{
            position: relative;
            ul{
                  width: 67px;
                  padding: 3px 10px;
                  position: absolute;
                  top: 20px;
                  right: 0;
                  background-color: rgba(255, 255, 255, 0.3);
                  border-radius: 4px;
                  li{
                        cursor: pointer;
                        i{
                              margin-right: 5px;
                        }
                  }
                 
            }
      }
}
.my-date-picker{
      background-color: rgba(255, 255, 255, 0.5);
      .ant-calendar{
            background-color: rgba(255, 255, 255, 0.3);
      }
}

</style>
