������ο���ҳ��
https://blog.csdn.net/yaoyefengchen/article/details/79427475

���ܣ�
��¼΢�ţ�����������Ů���������ѵ���λ�÷ֲ����Լ�ǩ����Ϣ��ͬʱ�Կ��ӻ���ʽչʾ������


#########
�����Ľ�����ݣ�����������ҳ���п��ӻ�չʾ
http://echarts.baidu.com/examples/editor.html?c=map-polygon

option = {
    title : {
        text: '΢�ź����Ա����',
        subtext: '��ʵ����',
        x:'center'
    },
    tooltip : {
        trigger: 'item',
        formatter: "{a} <br/>{b} : {c} ({d}%)"
    },
    legend: {
        orient : 'vertical',
        x : 'left',
        data:['����','Ů��']
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
            name:'������Դ',
            type:'pie',
            radius : '55%',
            center: ['50%', '60%'],
            data:[
                {value:170, name:'����'},
                {value:143, name:'Ů��'}
            ]
        }
    ]
}; 

##########
option = {
    title : {
        text: '΢�ź���ȫ���ֲ�ͼ',
        subtext: '��ʵ����',
        x:'center'
    },
    tooltip : {
        trigger: 'item'
    },
    legend: {
        orient: 'vertical',
        x:'left',
        data:['��������']
    },
    dataRange: {
        min: 0,
        max: 100,
        x: 'left',
        y: 'bottom',
        text:['��','��'],           // �ı���Ĭ��Ϊ��ֵ�ı�
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
            name: '��������',
            type: 'map',
            mapType: 'china',
            roam: false,
            itemStyle:{
                normal:{label:{show:true}},
                emphasis:{label:{show:true}}
            },
            data:[
{'name': '����', 'value': 26}, 
{'name': '�Ϻ�', 'value': 10}, 
{'name': '���', 'value': 4}, 
{'name': '����', 'value': 8}, 
{'name': '�ӱ�', 'value': 3}, 
{'name': 'ɽ��', 'value': 8}, 
{'name': '����', 'value': 5}, 
{'name': '����', 'value': 6}, 
{'name': '������', 'value': 0}, 
{'name': '����', 'value': 9}, 
{'name': '����', 'value': 1}, 
{'name': '�ຣ', 'value': 0}, 
{'name': 'ɽ��', 'value': 11}, 
{'name': '����', 'value': 1}, 
{'name': '�㽭', 'value': 8}, 
{'name': '̨��', 'value': 0}, 
{'name': '����', 'value': 7}, 
{'name': '����', 'value': 7}, 
{'name': '����', 'value': 6}, 
{'name': '����', 'value': 0}, 
{'name': '����', 'value': 13}, 
{'name': '����', 'value': 2}, 
{'name': '�㶫', 'value': 12}, 
{'name': '����', 'value': 1}, 
{'name': '�Ĵ�', 'value': 11}, 
{'name': '����', 'value': 2}, 
{'name': '����', 'value': 1}, 
{'name': '���ɹ�', 'value': 1}, 
{'name': '�½�', 'value': 0}, 
{'name': '����', 'value': 0}, 
{'name': '����', 'value': 1}, 
{'name': '����', 'value': 0}, 
{'name': '���', 'value': 1}, 
{'name': '����', 'value': 1}
            ]
        }
    ]
};


�ο���
pip��װWordcloud�ɲο���ҳ https://blog.csdn.net/u011389474/article/details/60764926/

