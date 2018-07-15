<template>
<div>


    <TreeBrowser
        :node="root"
        :new_boss="new_boss"
        v-on:next_man="next_man"
    />
</div>
</template>
<script>
    export default {
        props:['peoples','new_boss'],
data(){
    return{

        root:{},
        i:0,
        name:'',
    }
},
        methods:{
            next_man(data){
                axios.post(`/next_man`, {
                    name:data[1]}).then(response => {
                        if(response.data!='')
                {
                    switch (data[0]) {
                        case 1:
                            var name;
                            this.root['children'].filter(function (item) {
                                if (item.name == data[2][0]) {
                                    item.children = response.data;
                                    name =item.name+' '+item.patronymic+' '+item.surname;
                                }
//
                            });
                            alert('завантажити підлеглих ' + name+'?');
                            break;
                        case 2:
                            var name;
                            this.root['children'].filter(function (item) {
                                if (item.name == data[2][1]) {
                                    item['children'].filter(function (iten) {
                                        if (iten.name == data[2][0]) {
                                            iten.children = response.data;
                                            name =iten.name+' '+iten.patronymic+' '+iten.surname;

                                        }
                                    });
                                }
                            });
                            alert('завантажити підлеглих ' + name+'?');
                            break;
                        case 3:
                            var name;
                            this.root['children'].filter(function (item) {
                                if (item.name == data[2][2]) {
                                    item['children'].filter(function (iten) {
                                        if (iten.name == data[2][1]) {
                                            iten['children'].filter(function (itez) {
                                                if (itez.name == data[2][0]) {
                                                    itez.children = response.data;


                                                     name =itez.name+' '+itez.patronymic+' '+itez.surname;
                                                }
                                            });
                                        }
                                    });
                                }
                            });
                            alert('завантажити підлеглих ' + name+'?');
                            break;
                        case 4:
                            var name;
                            this.root['children'].filter(function (item) {
                                if (item.name == data[2][3]) {
                                    item['children'].filter(function (iten) {
                                        if (iten.name == data[2][2]) {
                                            iten['children'].filter(function (itez) {
                                                if (itez.name == data[2][1]) {
                                                    itez['children'].filter(function (itex) {
                                                        if (itex.name == data[2][0]) {
                                                            itex.children = response.data;
                                                             name =itex.name+' '+itex.patronymic+' '+itex.surname;
//                                                            this.name=itex.name;

                                                        }
                                                    });
                                                }
                                            });
                                        }
                                    });
                                }
                            });
                            alert('завантажити підлеглих ' + name+'?');
                            break;
                        case 5:
                            var name;
                            this.root['children'].filter(function (item) {
                                if (item.name == data[2][4]) {
                                    item['children'].filter(function (iteq) {
                                        if (iteq.name == data[2][3]) {
                                            iteq['children'].filter(function (iten) {
                                                if (iten.name == data[2][2]) {
                                                    iten['children'].filter(function (itez) {
                                                        if (itez.name == data[2][1]) {
                                                            itez['children'].filter(function (itex) {
                                                                if (itex.name == data[2][0]) {
                                                                    itex.children = response.data;
                                                                    name =itex.name+' '+itex.patronymic+' '+itex.surname;

                                                                }
                                                            });
                                                        }
                                                    });
                                                }
                                            });
                                        }
                                    });
                                }
                            });
                            alert('завантажити підлеглих ' + name+'?');
                            break;
                        case 6:
                            var name;
                            this.root['children'].filter(function (item) {
                                if (item.name == data[2][5]) {
                                    item['children'].filter(function (itew) {
                                        if (itew.name == data[2][4]) {
                                            itew['children'].filter(function (iteq) {
                                                if (iteq.name == data[2][3]) {
                                                    iteq['children'].filter(function (iten) {
                                                        if (iten.name == data[2][2]) {
                                                            iten['children'].filter(function (itez) {
                                                                if (itez.name == data[2][1]) {
                                                                    itez['children'].filter(function (itex) {
                                                                        if (itex.name == data[2][0]) {
                                                                            itex.children = response.data;
                                                                            name =itex.name+' '+itex.patronymic+' '+itex.surname;

                                                                        }
                                                                    });
                                                                }
                                                            });
                                                        }
                                                    });
                                                }
                                            });
                                        }
                                    });
                                }
                            });
                            alert('завантажити підлеглих ' + name+'?');
                            break;
                        case 7:
                            var name;
                            this.root['children'].filter(function (item) {
                                if (item.name == data[2][6]) {
                                    item['children'].filter(function (itee) {
                                        if (itee.name == data[2][5]) {
                                            itee['children'].filter(function (itew) {
                                                if (itew.name == data[2][4]) {
                                                    itew['children'].filter(function (iteq) {
                                                        if (iteq.name == data[2][3]) {
                                                            iteq['children'].filter(function (iten) {
                                                                if (iten.name == data[2][2]) {
                                                                    iten['children'].filter(function (itez) {
                                                                        if (itez.name == data[2][1]) {
                                                                            itez['children'].filter(function (itex) {
                                                                                if (itex.name == data[2][0]) {
                                                                                    itex.children = response.data;
                                                                                    name =itex.name+' '+itex.patronymic+' '+itex.surname;

                                                                                }
                                                                            });
                                                                        }
                                                                    });
                                                                }
                                                            });
                                                        }
                                                    });
                                                }
                                            });
                                        }
                                    });
                                }});
                            alert('завантажити підлеглих ' + name+'?');
                            break;
                        case 8:
                            var name;
                            this.root['children'].filter(function (item) {
                                if (item.name == data[2][7]) {
                                    item['children'].filter(function (iter) {
                                        if (iter.name == data[2][6]) {
                                            iter['children'].filter(function (itee) {
                                                if (itee.name == data[2][5]) {
                                                    itee['children'].filter(function (itew) {
                                                        if (itew.name == data[2][4]) {
                                                            itew['children'].filter(function (iteq) {
                                                                if (iteq.name == data[2][3]) {
                                                                    iteq['children'].filter(function (iten) {
                                                                        if (iten.name == data[2][2]) {
                                                                            iten['children'].filter(function (itez) {
                                                                                if (itez.name == data[2][1]) {
                                                                                    itez['children'].filter(function (itex) {
                                                                                        if (itex.name == data[2][0]) {
                                                                                            itex.children = response.data;
                                                                                            name =itex.name+' '+itex.patronymic+' '+itex.surname;

                                                                                        }
                                                                                    });
                                                                                }
                                                                            });
                                                                        }
                                                                    });
                                                                }
                                                            });
                                                        }
                                                    });
                                                }
                                            });
                                        }
                                    });
                                }});
                            alert('завантажити підлеглих ' + name+'?');
                            break;
                        case 9:
                            var name;
                            this.root['children'].filter(function (item) {
                                if (item.name == data[2][8]) {
                                    item['children'].filter(function (itet) {
                                        if (itet.name == data[2][7]) {
                                            itet['children'].filter(function (iter) {
                                                if (iter.name == data[2][6]) {
                                                    iter['children'].filter(function (itee) {
                                                        if (itee.name == data[2][5]) {
                                                            itee['children'].filter(function (itew) {
                                                                if (itew.name == data[2][4]) {
                                                                    itew['children'].filter(function (iteq) {
                                                                        if (iteq.name == data[2][3]) {
                                                                            iteq['children'].filter(function (iten) {
                                                                                if (iten.name == data[2][2]) {
                                                                                    iten['children'].filter(function (itez) {
                                                                                        if (itez.name == data[2][1]) {
                                                                                            itez['children'].filter(function (itex) {
                                                                                                if (itex.name == data[2][0]) {
                                                                                                    itex.children = response.data;
                                                                                                    name =itex.name+' '+itex.patronymic+' '+itex.surname;

                                                                                                }
                                                                                            });
                                                                                        }
                                                                                    });
                                                                                }
                                                                            });
                                                                        }
                                                                    });
                                                                }
                                                            });
                                                        }
                                                    });
                                                }
                                            });
                                        }
                                    });
                                }});
                            alert('завантажити підлеглих ' + name+'?');
                            break;
                        case 10:
                            var name;
                            this.root['children'].filter(function (item) {
                                if (item.name == data[2][9]) {
                                    item['children'].filter(function (itey) {
                                        if (itey.name == data[2][8]) {
                                            itey['children'].filter(function (itet) {
                                                if (itet.name == data[2][7]) {
                                                    itet['children'].filter(function (iter) {
                                                        if (iter.name == data[2][6]) {
                                                            iter['children'].filter(function (itee) {
                                                                if (itee.name == data[2][5]) {
                                                                    itee['children'].filter(function (itew) {
                                                                        if (itew.name == data[2][4]) {
                                                                            itew['children'].filter(function (iteq) {
                                                                                if (iteq.name == data[2][3]) {
                                                                                    iteq['children'].filter(function (iten) {
                                                                                        if (iten.name == data[2][2]) {
                                                                                            iten['children'].filter(function (itez) {
                                                                                                if (itez.name == data[2][1]) {
                                                                                                    itez['children'].filter(function (itex) {
                                                                                                        if (itex.name == data[2][0]) {
                                                                                                            itex.children = response.data;
                                                                                                            name =itex.name+' '+itex.patronymic+' '+itex.surname;

                                                                                                        }
                                                                                                    });
                                                                                                }
                                                                                            });
                                                                                        }
                                                                                    });
                                                                                }
                                                                            });
                                                                        }
                                                                    });
                                                                }
                                                            });
                                                        }
                                                    });
                                                }
                                            });
                                        }
                                    });
                                }});
                            alert('завантажити підлеглих ' + name+'?');
                            break;
                        default:
                            alert('системою передюачно іерархию до 10 рівнів');
                    }
//                    this.root['children'][0].children=response.data;
       ;
                }else {
                            alert('в даного співробітника нема підлеглих')
                }
            });
console.log(data[2]);
            },

        },
        created: function () {
           this.root=this.peoples;


        }


    }
</script>
<style>

</style>


















































<!--<template>-->

    <!--<div>-->
<!--{{category}}-->
        <!--<div>-->
            <!--<ol>-->
                <!--<tree :nodes="category" :show_checkbox="show_checkbox" :depth="0" v-on:push_people="push_people"></tree>-->
            <!--</ol>-->
        <!--</div>-->


        <!--<button v-on:click="test" >ok</button>-->


    <!--</div>-->


<!--</template>-->






<!--<script>-->


    <!--export default {-->
        <!--props: ['peoples'],-->
        <!--data(){-->
            <!--return {-->

                <!--id: '',-->
                <!--category: [],-->
                <!--show_checkbox: false,-->
                <!--subcaregory: [],-->
                <!--where: '',-->
                <!--who: '',-->
                <!--show_ok: false,-->
                <!--idd: 0,-->
                <!--iddd: 0,-->
                <!--categor_set:[],-->


            <!--}-->

        <!--},-->
        <!--methods: {-->

<!--test:function () {-->

    <!--var finalObj = this.category.concat({ "111": [ { "id": 22, "name": "qqqqqqqq", "patronymic": "Михайлович", "surname": "Ящук", "boss": 0, "position": "головний иректор", "salary": 999999.99, "name_img": null, "created_at": null, "updated_at": null } ]});-->


    <!--this.category = finalObj;-->
<!--//    this.category.push('aaaaaaaaaaaaaaaaaaaaaaaaaaaa');-->
<!--},-->
            <!--push_people(data){-->
<!--//                this.category.push({ "0": [ { "id": 22, "name": "Вася", "patronymic": "Михайлович", "surname": "Ящук", "boss": 0, "position": "головний иректор", "salary": 999999.99, "name_img": null, "created_at": null, "updated_at": null } ]});-->
<!--//                axios.post(`/test`, {id:data[0]}).then(response => {-->

<!--//alert(response.data);-->
<!--//                    this.category.push(response.data);-->


<!--//                });-->



            <!--},-->

        <!--},-->
        <!--created: function () {-->
            <!--this.category = this.peoples;-->
        <!--}-->


    <!--}-->




<!--</script>-->
