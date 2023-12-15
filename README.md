# code46
package csgw;  
public class Test {
    public static void main(String[] args){
        //创建商品
        Goods g1=new Goods("油饼");
        Goods g2=new Goods("豆浆机");
        Goods g3=new Goods("黄豆");

        Goods g4=new Goods("自然堂");
        Goods g5=new Goods("洁柔");
        //创建超市
        Supermarket m=new Supermarket();
        m.setName("华润万家");
        m.setStore(new Goods[]{g4,g5});

        Supermarket s=new Supermarket();
        s.setName("家乐福");
        s.setStore(new Goods[]{g1,g2,g3});//给s超市的库存赋值。
        //顾客
        Person c=new Person();
        c.setName("小寒");
        //购物行为
        Goods go1=c.shopping(m,"豆浆机");
        if(go1!=null) {
          System.out.println(c.getName() + "在" + m.getName() + "买到了"+go1.getName()+"。");
         }else {
          System.out.println(c.getName() + "在" + m.getName() + ",什么也没有买到。");
         }

       /* Goods go2=c.shopping(s,"豆浆机");
        if(go2!=null) {
            System.out.println(c.getName() + "在" + s.getName() + "买到了"+go2.getName());
        }else {
            System.out.println(c.getName() + "在" + s.getName() + ",什么也没有买到。");
        }

        */
    }

}
