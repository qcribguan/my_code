本程序参考网页：
https://blog.csdn.net/yaoyefengchen/article/details/79427475

功能：
登录微信，分析好友男女比例，好友地理位置分布，以及签名信息；同时以可视化方式展示出来。


#########
分析的结果数据，可在以下网页进行可视化展示
http://echarts.baidu.com/examples/editor.html?c=map-polygon

option = {
    title : {
        text: '微信好友性别比例',
        subtext: '真实数据',
        x:'center'
    },
    tooltip : {
        trigger: 'item',
        formatter: "{a} <br/>{b} : {c} ({d}%)"
    },
    legend: {
        orient : 'vertical',
        x : 'left',
        data:['男性','女性']
    },
    toolbox: {
        show : true,
        feature : {
            mark : {show: true},
            dataView : {show: true, readOnly: false},
            magicType : {
                show: true, 
                type: ['pie', 'funnel'],
                option: {
                    funnel: {
                        x: '25%',
                        width: '50%',
                        funnelAlign: 'left',
                        max: 1548
                    }
                }
            },
            restore : {show: true},
            saveAsImage : {show: true}
        }
    },
    calculable : true,
    series : [
        {
            name:'访问来源',
            type:'pie',
            radius : '55%',
            center: ['50%', '60%'],
            data:[
                {value:170, name:'男性'},
                {value:143, name:'女性'}
            ]
        }
    ]
}; 

##########
option = {
    title : {
        text: '微信好友全国分布图',
        subtext: '真实数据',
        x:'center'
    },
    tooltip : {
        trigger: 'item'
    },
    legend: {
        orient: 'vertical',
        x:'left',
        data:['好友数量']
    },
    dataRange: {
        min: 0,
        max: 100,
        x: 'left',
        y: 'bottom',
        text:['高','低'],           // 文本，默认为数值文本
        calculable : true
    },
    toolbox: {
        show: true,
        orient : 'vertical',
        x: 'right',
        y: 'center',
        feature : {
            mark : {show: true},
            dataView : {show: true, readOnly: false},
            restore : {show: true},
            saveAsImage : {show: true}
        }
    },
    roamController: {
        show: true,
        x: 'right',
        mapTypeControl: {
            'china': true
        }
    },
    series : [
        {
            name: '好友数量',
            type: 'map',
            mapType: 'china',
            roam: false,
            itemStyle:{
                normal:{label:{show:true}},
                emphasis:{label:{show:true}}
            },
            data:[
{'name': '北京', 'value': 26}, 
{'name': '上海', 'value': 10}, 
{'name': '天津', 'value': 4}, 
{'name': '重庆', 'value': 8}, 
{'name': '河北', 'value': 3}, 
{'name': '山西', 'value': 8}, 
{'name': '吉林', 'value': 5}, 
{'name': '辽宁', 'value': 6}, 
{'name': '黑龙江', 'value': 0}, 
{'name': '陕西', 'value': 9}, 
{'name': '甘肃', 'value': 1}, 
{'name': '青海', 'value': 0}, 
{'name': '山东', 'value': 11}, 
{'name': '福建', 'value': 1}, 
{'name': '浙江', 'value': 8}, 
{'name': '台湾', 'value': 0}, 
{'name': '河南', 'value': 7}, 
{'name': '湖北', 'value': 7}, 
{'name': '湖南', 'value': 6}, 
{'name': '江西', 'value': 0}, 
{'name': '江苏', 'value': 13}, 
{'name': '安徽', 'value': 2}, 
{'name': '广东', 'value': 12}, 
{'name': '海南', 'value': 1}, 
{'name': '四川', 'value': 11}, 
{'name': '贵州', 'value': 2}, 
{'name': '云南', 'value': 1}, 
{'name': '内蒙古', 'value': 1}, 
{'name': '新疆', 'value': 0}, 
{'name': '宁夏', 'value': 0}, 
{'name': '广西', 'value': 1}, 
{'name': '西藏', 'value': 0}, 
{'name': '香港', 'value': 1}, 
{'name': '澳门', 'value': 1}
            ]
        }
    ]
};


参考：
pip安装Wordcloud可参考网页 https://blog.csdn.net/u011389474/article/details/60764926/

