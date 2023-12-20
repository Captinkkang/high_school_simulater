<script lang="ts">
  
    const high = {
        "고잔고":{"full":398,"name":"고잔고","count":0},
        "송호고":{"full":392,"name":"송호고","count":0},
        "경안고":{"full":415,"name":"경안고","count":0},
        "성안고":{"full":400,"name":"성안고","count":0},
        "상록고":{"full":404,"name":"상록고","count":0},
        "안산고":{"full":255,"name":"안산고","count":0},
        "성포고":{"full":383,"name":"성포고","count":0},
        "광덕고":{"full":340,"name":"광덕고","count":0},
        "양지고":{"full":354,"name":"양지고","count":0},
        "강서고":{"full":378,"name":"강서고","count":0},
        "선부고":{"full":338,"name":"선부고","count":0},
        "단원고":{"full":335,"name":"단원고","count":0},
        "부곡고":{"full":380,"name":"부곡고","count":0},
        "초지고":{"full":336,"name":"초지고","count":0},
        "대부고":{"full":118,"name":"대부고","count":0},
        "신길고":{"full":353,"name":"신길고","count":0},
        "원곡고":{"full":392,"name":"원곡고","count":0},
        
    }

    const schools = {
        "local":{"st":high.고잔고,"nd":high.송호고,"rd":high.성안고,"th":high.양지고,"fth":high.경안고},
        "area":{"st":high.고잔고,"nd":high.경안고,"rd":high.안산고,"th":high.광덕고,"fth":high.송호고,"sth":high.성안고,"seth":high.부곡고,"eth":high.성포고,"nth":high.상록고}
    }
    
    const middle = {
        "중앙중":{"class_num":9,"name":"중앙중","full":10,"1or2":1,"schools": {
            "local":{"st":high.경안고,"nd":high.성포고,"rd":high.고잔고,"th":high.송호고,"fth":high.광덕고},
            "area":{"st":high.경안고,"nd":high.성포고,"rd":high.고잔고,"th":high.송호고,"fth":high.광덕고,"sth":high.성안고,"seth":high.상록고,"eth":high.부곡고,"nth":high.안산고}
        }},
        "단원중":{"class_num":6,"name":"단원중","full":10,"1or2":2,"schools": {
            "local":{"st":high.단원고,"nd":high.경안고,"rd":high.강서고,"th":high.양지고,"fth":high.초지고},
            "area":{"st":high.단원고,"nd":high.강서고,"rd":high.양지고,"th":high.초지고,"fth":high.원곡고,"sth":high.선부고,"seth":high.신길고,"eth":high.대부고,"nth":""}
        }},
        "양지중":{"class_num":11,"name":"양지중","full":10,"1or2":1,"schools": {
            "local":{"st":high.고잔고,"nd":high.성안고,"rd":high.송호고,"th":high.양지고,"fth":high.경안고},
            "area":{"st":high.고잔고,"nd":high.성안고,"rd":high.송호고,"th":high.경안고,"fth":high.성포고,"sth":high.광덕고,"seth":high.상록고,"eth":high.부곡고,"nth":high.안산고}
        }},
        "성안중":{"class_num":6,"name":"성안중","full":10,"1or2":1,"schools": {
            "local":{"st":high.성안고,"nd":high.송호고,"rd":high.고잔고,"th":high.양지고,"fth":high.성포고},
            "area":{"st":high.성안고,"nd":high.송호고,"rd":high.고잔고,"th":high.성포고,"fth":high.경안고,"sth":high.상록고,"seth":high.광덕고,"eth":high.부곡고,"nth":high.안산고}
        }},
        "초지중":{"class_num":6,"name":"초지중","full":10,"1or2":2,"schools": {
            "local":{"st":high.초지고,"nd":high.양지고,"rd":high.고잔고,"th":high.단원고,"fth":high.경안고},
            "area":{"st":high.초지고,"nd":high.양지고,"rd":high.단원고,"th":high.강서고,"fth":high.원곡고,"sth":high.선부고,"seth":high.신길고,"eth":high.대부고,"nth":""}
        }},
        "해양중":{"class_num":6,"name":"해양중","full":10,"1or2":2,"schools": {
            "local":{"st":high.양지고,"nd":high.고잔고,"rd":high.초지고,"th":high.성안고,"fth":high.송호고},
            "area":{"st":high.양지고,"nd":high.초지고,"rd":high.단원고,"th":high.강서고,"fth":high.원곡고,"sth":high.선부고,"seth":high.신길고,"eth":high.대부고,"nth":""}
        }},
        "송호중":{"class_num":7,"name":"송호중","full":10,"1or2":1,"schools": {
            "local":{"st":high.송호고,"nd":high.고잔고,"rd":high.성안고,"th":high.양지고,"fth":high.경안고},
            "area":{"st":high.송호고,"nd":high.고잔고,"rd":high.성안고,"th":high.경안고,"fth":high.성포고,"sth":high.광덕고,"seth":high.상록고,"eth":high.부곡고,"nth":high.안산고}
        }},
        "별망중":{"class_num":5,"name":"별망중","full":10,"1or2":2,"schools": {
            "local":{"st":high.초지고,"nd":high.양지고,"rd":high.고잔고,"th":high.단원고,"fth":high.강서고},
            "area":{"st":high.초지고,"nd":high.양지고,"rd":high.단원고,"th":high.강서고,"fth":high.원곡고,"sth":high.선부고,"seth":high.신길고,"eth":high.대부고,"nth":""}
        }},
        "석호중":{"class_num":3,"name":"석호중","full":10,"1or2":1,"schools": {
            "local":{"st":high.성안고,"nd":high.상록고,"rd":high.송호고,"th":high.고잔고,"fth":high.성포고},
            "area":{"st":high.성안고,"nd":high.상록고,"rd":high.송호고,"th":high.고잔고,"fth":high.성포고,"sth":high.경안고,"seth":high.광덕고,"eth":high.부곡고,"nth":high.안산고}
        }},
        "시곡중":{"class_num":10,"name":"시곡중","full":10,"1or2":1,"schools": {
            "local":{"st":high.성안고,"nd":high.상록고,"rd":high.송호고,"th":high.고잔고,"fth":high.양지고},
            "area":{"st":high.성안고,"nd":high.상록고,"rd":high.송호고,"th":high.고잔고,"fth":high.경안고,"sth":high.성포고,"seth":high.광덕고,"eth":high.부곡고,"nth":high.안산고}
        }},
        "선부중":{"class_num":6,"name":"선부중","full":10,"1or2":2,"schools": {
            "local":{"st":high.강서고,"nd":high.원곡고,"rd":high.단원고,"th":high.선부고,"fth":high.경안고},
            "area":{"st":high.강서고,"nd":high.원곡고,"rd":high.단원고,"th":high.선부고,"fth":high.초지고,"sth":high.양지고,"seth":high.신길고,"eth":high.대부고,"nth":""}
        }},
        "상록중":{"class_num":6,"name":"상록중","full":10,"1or2":1,"schools": {
            "local":{"st":high.상록고,"nd":high.성안고,"rd":high.송호고,"th":high.고잔고,"fth":high.성포고},
            "area":{"st":high.상록고,"nd":high.성안고,"rd":high.송호고,"th":high.고잔고,"fth":high.성포고,"sth":high.경안고,"seth":high.광덕고,"eth":high.부곡고,"nth":high.안산고}
        }},
        "반월중":{"class_num":4,"name":"반월중","full":10,"1or2":1,"schools": {
            "local":{"st":high.상록고,"nd":high.송호고,"rd":high.성안고,"th":high.성포고,"fth":high.고잔고},
            "area":{"st":high.상록고,"nd":high.송호고,"rd":high.성안고,"th":high.성포고,"fth":high.고잔고,"sth":high.광덕고,"seth":high.경안고,"eth":high.부곡고,"nth":high.안산고}
        }},
        "이호중":{"class_num":9,"name":"이호중","full":10,"1or2":1,"schools": {
            "local":{"st":high.상록고,"nd":high.성안고,"rd":high.송호고,"th":high.고잔고,"fth":high.경안고},
            "area":{"st":high.상록고,"nd":high.성안고,"rd":high.송호고,"th":high.고잔고,"fth":high.경안고,"sth":high.성포고,"seth":high.광덕고,"eth":high.부곡고,"nth":high.안산고}
        }},
        "부곡중":{"class_num":5,"name":"부곡중","full":10,"1or2":1,"schools": {
            "local":{"st":high.성포고,"nd":high.부곡고,"rd":high.경안고,"th":high.송호고,"fth":high.광덕고},
            "area":{"st":high.성포고,"nd":high.부곡고,"rd":high.경안고,"th":high.송호고,"fth":high.광덕고,"sth":high.고잔고,"seth":high.성안고,"eth":high.상록고,"nth":high.안산고}
        }},
        "경수중":{"class_num":5,"name":"경수중","full":10,"1or2":1,"schools": {
            "local":{"st":high.성포고,"nd":high.경안고,"rd":high.광덕고,"th":high.송호고,"fth":high.고잔고},
            "area":{"st":high.성포고,"nd":high.성포고,"rd":high.광덕고,"th":high.송호고,"fth":high.고잔고,"sth":high.성안고,"seth":high.부곡고,"eth":high.상록고,"nth":high.안산고}
        }},
        "광덕중":{"class_num":2,"name":"광덕중","full":10,"1or2":1,"schools": {
            "local":{"st":high.광덕고,"nd":high.부곡고,"rd":high.성포고,"th":high.경안고,"fth":high.송호고},
            "area":{"st":high.광덕고,"nd":high.부곡고,"rd":high.성포고,"th":high.경안고,"fth":high.송호고,"sth":high.고잔고,"seth":high.성안고,"eth":high.상록고,"nth":high.안산고}
        }},
        "성호중":{"class_num":8,"name":"성호중","full":10,"1or2":1,"schools": {
            "local":{"st":high.상록고,"nd":high.송호고,"rd":high.성안고,"th":high.고잔고,"fth":high.성포고},
            "area":{"st":high.상록고,"nd":high.송호고,"rd":high.성안고,"th":high.고잔고,"fth":high.성포고,"sth":high.부곡고,"seth":high.경안고,"eth":high.광덕고,"nth":high.안산고}
        }},
        "성포중":{"class_num":5,"name":"성포중","full":10,"1or2":1,"schools": {
            "local":{"st":high.광덕고,"nd":high.부곡고,"rd":high.성포고,"th":high.경안고,"fth":high.송호고},
            "area":{"st":high.광덕고,"nd":high.부곡고,"rd":high.성포고,"th":high.경안고,"fth":high.송호고,"sth":high.고잔고,"seth":high.성안고,"eth":high.상록고,"nth":high.안산고}
        }},
        "본오중":{"class_num":9,"name":"본오중","full":10,"1or2":1,"schools": {
            "local":{"st":high.상록고,"nd":high.성안고,"rd":high.송호고,"th":high.고잔고,"fth":high.성포고},
            "area":{"st":high.상록고,"nd":high.성안고,"rd":high.송호고,"th":high.고잔고,"fth":high.성포고,"sth":high.경안고,"seth":high.부곡고,"eth":high.광덕고,"nth":high.안산고}
        }},
        "관산중":{"class_num":6,"name":"관산중","full":10,"1or2":2,"schools": {
            "local":{"st":high.원곡고,"nd":high.신길고,"rd":high.강서고,"th":high.단원고,"fth":high.선부고},
            "area":{"st":high.원곡고,"nd":high.신길고,"rd":high.강서고,"th":high.단원고,"fth":high.선부고,"sth":high.초지고,"seth":high.양지고,"eth":high.대부고,"nth":""}
        }},
        "대부중":{"class_num":1,"name":"대부중","full":10,"1or2":2,"schools": {
            "local":{"st":high.대부고,"nd":high.신길고,"rd":high.선부고,"th":high.원곡고,"fth":high.강서고},
            "area":{"st":high.대부고,"nd":high.신길고,"rd":high.선부고,"th":high.원곡고,"fth":high.강서고,"sth":high.단원고,"seth":high.초지고,"eth":high.양지고,"nth":""}
        }},
        "석수중":{"class_num":5,"name":"석수중","full":10,"1or2":2,"schools": {
            "local":{"st":high.강서고,"nd":high.원곡고,"rd":high.단원고,"th":high.선부고,"fth":high.신길고},
            "area":{"st":high.강서고,"nd":high.원곡고,"rd":high.단원고,"th":high.선부고,"fth":high.신길고,"sth":high.초지고,"seth":high.양지고,"eth":high.대부고,"nth":""}
        }},
        "신길중":{"class_num":8,"name":"신길중","full":10,"1or2":2,"schools": {
            "local":{"st":high.신길고,"nd":high.원곡고,"rd":high.선부고,"th":high.강서고,"fth":high.단원고},
            "area":{"st":high.신길고,"nd":high.원곡고,"rd":high.선부고,"th":high.강서고,"fth":high.단원고,"sth":high.초지고,"seth":high.양지고,"eth":high.대부고,"nth":""}
        }},
        "선일중":{"class_num":3,"name":"선일중","full":10,"1or2":2,"schools": {
            "local":{"st":high.원곡고,"nd":high.강서고,"rd":high.선부고,"th":high.신길고,"fth":high.단원고},
            "area":{"st":high.원곡고,"nd":high.강서고,"rd":high.선부고,"th":high.신길고,"fth":high.단원고,"sth":high.초지고,"seth":high.양지고,"eth":high.대부고,"nth":""}
        }},
        "와동중":{"class_num":5,"name":"와동중","full":10,"1or2":2,"schools": {
            "local":{"st":high.단원고,"nd":high.강서고,"rd":high.경안고,"th":high.원곡고,"fth":high.선부고},
            "area":{"st":high.단원고,"nd":high.강서고,"rd":high.원곡고,"th":high.선부고,"fth":high.신길고,"sth":high.초지고,"seth":high.양지고,"eth":high.대부고,"nth":""}
        }},
        "원곡중":{"class_num":11,"name":"원곡중","full":10,"1or2":2,"schools": {
            "local":{"st":high.원곡고,"nd":high.선부고,"rd":high.신길고,"th":high.강서고,"fth":high.단원고},
            "area":{"st":high.원곡고,"nd":high.선부고,"rd":high.신길고,"th":high.강서고,"fth":high.단원고,"sth":high.초지고,"seth":high.양지고,"eth":high.대부고,"nth":""}
        }},
        "원일중":{"class_num":8,"name":"원일중","full":10,"1or2":2,"schools": {
            "local":{"st":high.강서고,"nd":high.원곡고,"rd":high.선부고,"th":high.단원고,"fth":high.신길고},
            "area":{"st":high.강서고,"nd":high.원곡고,"rd":high.선부고,"th":high.단원고,"fth":high.신길고,"sth":high.초지고,"seth":high.양지고,"eth":high.대부고,"nth":""}
        },},
        "안산중":{"class_num":2,"name":"안산중","full":10,"1or2":1,"schools": {
            "local":{"st":high.안산고,"nd":high.성포고,"rd":high.부곡고,"th":high.광덕고,"fth":high.경안고},
            "area":{"st":high.안산고,"nd":high.성포고,"rd":high.부곡고,"th":high.광덕고,"fth":high.경안고,"sth":high.송호고,"seth":high.고잔고,"eth":high.성안고,"nth":high.상록고}
        }},
        "해솔중":{"class_num":9,"name":"해솔중","full":10,"1or2":1,"schools": {
            "local":{"st":high.성안고,"nd":high.고잔고,"rd":high.송호고,"th":high.경안고,"fth":high.상록고},
            "area":{"st":high.성안고,"nd":high.고잔고,"rd":high.송호고,"th":high.경안고,"fth":high.상록고,"sth":high.부곡고,"seth":high.성포고,"eth":high.광덕고,"nth":high.안산고}
        }},
    }
    
    const pick = (school:string,room:number,id:number) => {
        let arr = Object.entries(middle)
        let aarr=[]
        let school_turn = []
        for(let i=0; i<arr.length; i++){
            aarr.push(arr[i][1])
        }
        for(let i=0; i<30; i++){
            let temp = Math.floor(Math.random()*aarr.length)
            school_turn.push(aarr[temp])
            aarr.splice(temp,1)
        }
        //위에는 학교 순서 정해서 배열에 저장하는 코드
        
        let brr = []
        let room_turn = []
        if(school === "중앙중"){
            for(let i=1; i<=middle.중앙중.class_num; i++){
                brr.push(i)
            }
            for(let i=0; i<middle.중앙중.class_num; i++){
                let temp = Math.floor(Math.random()*brr.length)
                room_turn.push(brr[temp])
                brr.splice(temp,1)
            }
        }else if(school === "단원중"){
            for(let i=1; i<=middle.단원중.class_num; i++){
                brr.push(i)
            }
            for(let i=0; i<middle.단원중.class_num; i++){
                let temp = Math.floor(Math.random()*brr.length)
                room_turn.push(brr[temp])
                brr.splice(temp,1)
            }
        }else if(school === "양지중"){
            for(let i=1; i<=middle.양지중.class_num; i++){
                brr.push(i)
            }
            for(let i=0; i<middle.양지중.class_num; i++){
                let temp = Math.floor(Math.random()*brr.length)
                room_turn.push(brr[temp])
                brr.splice(temp,1)
            }
        }else if(school === "성안중"){
            for(let i=1; i<=middle.성안중.class_num; i++){
                brr.push(i)
            }
            for(let i=0; i<middle.성안중.class_num; i++){
                let temp = Math.floor(Math.random()*brr.length)
                room_turn.push(brr[temp])
                brr.splice(temp,1)
            }
        }else if(school === "초지중"){
            for(let i=1; i<=middle.초지중.class_num; i++){
                brr.push(i)
            }
            for(let i=0; i<middle.초지중.class_num; i++){
                let temp = Math.floor(Math.random()*brr.length)
                room_turn.push(brr[temp])
                brr.splice(temp,1)
            }
        }else if(school === "해양중"){
            for(let i=1; i<=middle.해양중.class_num; i++){
                brr.push(i)
            }
            for(let i=0; i<middle.해양중.class_num; i++){
                let temp = Math.floor(Math.random()*brr.length)
                room_turn.push(brr[temp])
                brr.splice(temp,1)
            }
        }else if(school === "송호중"){
            for(let i=1; i<=middle.송호중.class_num; i++){
                brr.push(i)
            }
            for(let i=0; i<middle.송호중.class_num; i++){
                let temp = Math.floor(Math.random()*brr.length)
                room_turn.push(brr[temp])
                brr.splice(temp,1)
            }
        }else if(school === "별망중"){
            for(let i=1; i<=middle.별망중.class_num; i++){
                brr.push(i)
            }
            for(let i=0; i<middle.별망중.class_num; i++){
                let temp = Math.floor(Math.random()*brr.length)
                room_turn.push(brr[temp])
                brr.splice(temp,1)
            }
        }else if(school === "석호중"){
            for(let i=1; i<=middle.석호중.class_num; i++){
                brr.push(i)
            }
            for(let i=0; i<middle.석호중.class_num; i++){
                let temp = Math.floor(Math.random()*brr.length)
                room_turn.push(brr[temp])
                brr.splice(temp,1)
            }
        }else if(school === "시곡중"){
            for(let i=1; i<=middle.시곡중.class_num; i++){
                brr.push(i)
            }
            for(let i=0; i<middle.시곡중.class_num; i++){
                let temp = Math.floor(Math.random()*brr.length)
                room_turn.push(brr[temp])
                brr.splice(temp,1)
            }
        }else if(school === "선부중"){
            for(let i=1; i<=middle.선부중.class_num; i++){
                brr.push(i)
            }
            for(let i=0; i<middle.선부중.class_num; i++){
                let temp = Math.floor(Math.random()*brr.length)
                room_turn.push(brr[temp])
                brr.splice(temp,1)
            }
        }else if(school === "상록중"){
            for(let i=1; i<=middle.상록중.class_num; i++){
                brr.push(i)
            }
            for(let i=0; i<middle.상록중.class_num; i++){
                let temp = Math.floor(Math.random()*brr.length)
                room_turn.push(brr[temp])
                brr.splice(temp,1)
            }
        }else if(school === "반월중"){
            for(let i=1; i<=middle.반월중.class_num; i++){
                brr.push(i)
            }
            for(let i=0; i<middle.반월중.class_num; i++){
                let temp = Math.floor(Math.random()*brr.length)
                room_turn.push(brr[temp])
                brr.splice(temp,1)
            }
        }else if(school === "이호중"){
            for(let i=1; i<=middle.이호중.class_num; i++){
                brr.push(i)
            }
            for(let i=0; i<middle.이호중.class_num; i++){
                let temp = Math.floor(Math.random()*brr.length)
                room_turn.push(brr[temp])
                brr.splice(temp,1)
            }
        }else if(school === "부곡중"){
            for(let i=1; i<=middle.부곡중.class_num; i++){
                brr.push(i)
            }
            for(let i=0; i<middle.부곡중.class_num; i++){
                let temp = Math.floor(Math.random()*brr.length)
                room_turn.push(brr[temp])
                brr.splice(temp,1)
            }
        }else if(school === "경수중"){
            for(let i=1; i<=middle.경수중.class_num; i++){
                brr.push(i)
            }
            for(let i=0; i<middle.경수중.class_num; i++){
                let temp = Math.floor(Math.random()*brr.length)
                room_turn.push(brr[temp])
                brr.splice(temp,1)
            }
        }else if(school === "광덕중"){
            for(let i=1; i<=middle.광덕중.class_num; i++){
                brr.push(i)
            }
            for(let i=0; i<middle.광덕중.class_num; i++){
                let temp = Math.floor(Math.random()*brr.length)
                room_turn.push(brr[temp])
                brr.splice(temp,1)
            }
        }else if(school === "성호중"){
            for(let i=1; i<=middle.성호중.class_num; i++){
                brr.push(i)
            }
            for(let i=0; i<middle.성호중.class_num; i++){
                let temp = Math.floor(Math.random()*brr.length)
                room_turn.push(brr[temp])
                brr.splice(temp,1)
            }
        }else if(school === "성포중"){
            for(let i=1; i<=middle.성포중.class_num; i++){
                brr.push(i)
            }
            for(let i=0; i<middle.성포중.class_num; i++){
                let temp = Math.floor(Math.random()*brr.length)
                room_turn.push(brr[temp])
                brr.splice(temp,1)
            }
        }else if(school === "본오중"){
            for(let i=1; i<=middle.본오중.class_num; i++){
                brr.push(i)
            }
            for(let i=0; i<middle.본오중.class_num; i++){
                let temp = Math.floor(Math.random()*brr.length)
                room_turn.push(brr[temp])
                brr.splice(temp,1)
            }
        }else if(school === "관산중"){
            for(let i=1; i<=middle.관산중.class_num; i++){
                brr.push(i)
            }
            for(let i=0; i<middle.관산중.class_num; i++){
                let temp = Math.floor(Math.random()*brr.length)
                room_turn.push(brr[temp])
                brr.splice(temp,1)
            }
        }else if(school === "대부중"){
            for(let i=1; i<=middle.대부중.class_num; i++){
                brr.push(i)
            }
            for(let i=0; i<middle.대부중.class_num; i++){
                let temp = Math.floor(Math.random()*brr.length)
                room_turn.push(brr[temp])
                brr.splice(temp,1)
            }
        }else if(school === "석수중"){
            for(let i=1; i<=middle.석수중.class_num; i++){
                brr.push(i)
            }
            for(let i=0; i<middle.석수중.class_num; i++){
                let temp = Math.floor(Math.random()*brr.length)
                room_turn.push(brr[temp])
                brr.splice(temp,1)
            }
        }else if(school === "신길중"){
            for(let i=1; i<=middle.신길중.class_num; i++){
                brr.push(i)
            }
            for(let i=0; i<middle.신길중.class_num; i++){
                let temp = Math.floor(Math.random()*brr.length)
                room_turn.push(brr[temp])
                brr.splice(temp,1)
            }
        }else if(school === "선일중"){
            for(let i=1; i<=middle.선일중.class_num; i++){
                brr.push(i)
            }
            for(let i=0; i<middle.선일중.class_num; i++){
                let temp = Math.floor(Math.random()*brr.length)
                room_turn.push(brr[temp])
                brr.splice(temp,1)
            }
        }else if(school === "와동중"){
            for(let i=1; i<=middle.와동중.class_num; i++){
                brr.push(i)
            }
            for(let i=0; i<middle.와동중.class_num; i++){
                let temp = Math.floor(Math.random()*brr.length)
                room_turn.push(brr[temp])
                brr.splice(temp,1)
            }
        }else if(school === "원곡중"){
            for(let i=1; i<=middle.원곡중.class_num; i++){
                brr.push(i)
            }
            for(let i=0; i<middle.원곡중.class_num; i++){
                let temp = Math.floor(Math.random()*brr.length)
                room_turn.push(brr[temp])
                brr.splice(temp,1)
            }
        }else if(school === "원일중"){
            for(let i=1; i<=middle.원일중.class_num; i++){
                brr.push(i)
            }
            for(let i=0; i<middle.원일중.class_num; i++){
                let temp = Math.floor(Math.random()*brr.length)
                room_turn.push(brr[temp])
                brr.splice(temp,1)
            }
        }else if(school === "안산중"){
            for(let i=1; i<=middle.안산중.class_num; i++){
                brr.push(i)
            }
            for(let i=0; i<middle.안산중.class_num; i++){
                let temp = Math.floor(Math.random()*brr.length)
                room_turn.push(brr[temp])
                brr.splice(temp,1)
            }
        }else if(school === "해솔중"){
            for(let i=1; i<=middle.해솔중.class_num; i++){
                brr.push(i)
            }
            for(let i=0; i<middle.해솔중.class_num; i++){
                let temp = Math.floor(Math.random()*brr.length)
                room_turn.push(brr[temp])
                brr.splice(temp,1)
            }
        }
        //위에는 반 순서 뽑는 코드=>배열에 저장

        let crr = []
        let id_turn = []
        for(let i=1; i<=31; i++){
            crr.push(i)
        }
        for(let i=0; i<31; i++){
            let temp = Math.floor(Math.random()*crr.length)
            id_turn.push(crr[temp])
            crr.splice(temp,1)
        }
        //위에는 자기 번호 순서 뽑는 코드=>배열에 저장
        let rt;
        let ct;
        let mt;
        for(let i=1; i<=school_turn.length; i++){
            if(school_turn[i-1].name === school){
                rt = i
                //console.log(school_turn)
                alert(`${school_turn[i-1].name}는 ${i}번째 입니다.`)
            }
        }
        for(let i=1; i<=room_turn.length; i++){
            if(room_turn[i-1] === room){
                ct = i
                //console.log(room_turn)
                alert(`${room}반은 ${i}번째 입니다.`)
            }
        }
        for(let i=1; i<=id_turn.length; i++){
            if(id_turn[i-1] === id){
                mt = i
                //console.log(id_turn)
                alert(`당신의 순서는 ${i}번째 입니다.`)
            }
        }

        /*학교별로 기준이 되는 원서를 정해서 그 원서에 맞게 정한다.
        학생을 배열?로 저장한 뒤 자기 학교에 자기반, 자기 번호에 있는 학생에는 me라느 변수를 대신 push하고
        자기 차례가 되면 남는 자리에 안착 후 결과에 따라 여부칸을 빨간색, 초록색으로 표시
        high객체의 각각의 내부 객체에 있는 count와 full이 같으면 더이상 그 학교는 들어갈 수 없다
        만약 자신이 아무데에도 당첨되지 못했다면 자신이 작성한 schools 객체에 없는 다른 자리가 남는 학교중 랜덤으로 간다
        */
        for(let i=0; i<30; i++){
            //이거 멍창하게 for, if문 몇 십개 씩 않쓰게 차례 배열 안에도 학교 정보 객체를 넣자 근데 되는지는 모름
            let a = school_turn[i]
            let area = a.schools.area
            let local = a.schools.local
            if(typeof rt !== "number")return
            if(i === rt-1){
                //우리 학교 차례일 때
                if(a.name === school){
                    //우리학교 맞나 확인
                    //console.log(high,`${i}우리 학교 차례`)//알려주고
                    //console.log(a.class_num)
                    //alert("지금!")
                    for(let j=0; j<a.class_num; j++){
                        //학급 수만큼 반복
                        //console.log(j,"j다")
                        for(let k=0; k<31; k++){
                            //학급별 학생 수만큼 반복
                            //console.log(k,"k다")
                            //console.log(`${school} ${room_turn[j]}반 ${k+1}번`)//지금 누구인지 알려 주고
                            if(typeof ct === "number"&&typeof mt === "number"){
                                if(j === ct-1&&k === mt-1){
                                    //자기 반에서, 자기 순서인 경우
                                    console.log("1.여기까지 오긴 하나?")//확인 하고
                                    area = schools.area
                                    local = schools.local
                                    if(local.st.full !== local.st.count){
                                        local.st.count++
                                        alert(`지역내 배정, ${local.st.name}에 배정 되셨습니다.`)
                                    }else if(local.nd.full !== local.nd.count){
                                        local.nd.count++
                                        alert(`지역내 배정, ${local.nd.name}에 배정 되셨습니다.`)
                                    }else if(local.rd.full !== local.rd.count){
                                        local.rd.count++
                                        alert(`지역내 배정, ${local.rd.name}에 배정 되셨습니다.`)
                                    }else if(local.th.full !== local.th.count){
                                        local.th.count++
                                        alert(`지역내 배정, ${local.th.name}에 배정 되셨습니다.`)
                                    }else if(local.fth.full !== local.fth.count){
                                        local.fth.count++
                                        alert(`지역내 배정, ${local.fth.name}에 배정 되셨습니다.`)
                                    }else if(area.st.full !== area.st.count){
                                        area.st.count++
                                        alert(`학군내 배정, ${area.st.name}에 배정 되셨습니다.`)
                                    }else if(area.nd.full !== area.nd.count){
                                        area.nd.count++
                                        alert(`학군내 배정, ${area.nd.name}에 배정 되셨습니다.`)
                                    }else if(area.rd.full !== area.rd.count){
                                        area.rd.count++
                                        alert(`학군내 배정, ${area.rd.name}에 배정 되셨습니다.`)
                                    }else if(area.th.full !== area.th.count){
                                        area.th.count++
                                        alert(`학군내 배정, ${area.th.name}에 배정 되셨습니다.`)
                                    }else if(area.fth.full !== area.fth.count){
                                        area.fth.count++
                                        alert(`학군내 배정, ${area.fth.name}에 배정 되셨습니다.`)
                                    }else if(area.sth.full !== area.sth.count){
                                        area.sth.count++
                                        alert(`학군내 배정, ${area.sth.name}에 배정 되셨습니다.`)
                                    }else if(area.seth.full !== area.seth.count){
                                        area.seth.count++
                                        alert(`학군내 배정, ${area.seth.name}에 배정 되셨습니다.`)
                                    }else if(area.eth.full !== area.eth.count){
                                        area.eth.count++
                                        alert(`학군내 배정, ${area.eth.name}에 배정 되셨습니다.`)
                                    }else if(typeof area.nth !== "string"){
                                        if(area.nth.full !== area.nth.count){
                                            area.nth.count++
                                            alert(`학군내 배정, ${area.nth.name}에 배정 되셨습니다.`)
                                        }else alert(`유감스럽게도 지망하신 모든 학교가 모두 인원이 채워져 안산시에서 남는 학교에 배정 예정입니다.`)
                                    }
                                }
                            }else {
                                console.log(`${a.name} ${k}번`)
                                if(local.st.full !== local.st.count){
                                    local.st.count++
                                }else if(local.nd.full !== local.nd.count){
                                    local.nd.count++
                                }else if(local.rd.full !== local.rd.count){
                                    local.rd.count++
                                }else if(local.th.full !== local.th.count){
                                    local.th.count++
                                }else if(local.fth.full !== local.fth.count){
                                    local.fth.count++
                                }else if(area.st.full !== area.st.count){
                                    area.st.count++
                                }else if(area.nd.full !== area.nd.count){
                                    area.nd.count++
                                }else if(area.rd.full !== area.rd.count){
                                    area.rd.count++
                                }else if(area.th.full !== area.th.count){
                                    area.th.count++
                                }else if(area.fth.full !== area.fth.count){
                                    area.fth.count++
                                }else if(area.sth.full !== area.sth.count){
                                    area.sth.count++
                                }else if(area.seth.full !== area.seth.count){
                                    area.seth.count++
                                }else if(area.eth.full !== area.eth.count){
                                    area.eth.count++
                                }else if(typeof area.nth !== "string"){
                                    if(area.nth.full !== area.nth.count){
                                        area.nth.count++
                                    }
                                }
                            }
                            
                            
                        }
                    }
                }
            }else {
                for(let l=0; l<a.class_num; l++){
                    for(let p=0; p<31; p++){
                        //console.log(`${a.name} ${p}번`)
                        if(local.st.full !== local.st.count){
                            local.st.count++
                        }else if(local.nd.full !== local.nd.count){
                            local.nd.count++
                        }else if(local.rd.full !== local.rd.count){
                            local.rd.count++
                        }else if(local.th.full !== local.th.count){
                            local.th.count++
                        }else if(local.fth.full !== local.fth.count){
                            local.fth.count++
                        }else if(area.st.full !== area.st.count){
                            area.st.count++
                        }else if(area.nd.full !== area.nd.count){
                            area.nd.count++
                        }else if(area.rd.full !== area.rd.count){
                            area.rd.count++
                        }else if(area.th.full !== area.th.count){
                            area.th.count++
                        }else if(area.fth.full !== area.fth.count){
                            area.fth.count++
                        }else if(area.sth.full !== area.sth.count){
                            area.sth.count++
                        }else if(area.seth.full !== area.seth.count){
                            area.seth.count++
                        }else if(area.eth.full !== area.eth.count){
                            area.eth.count++
                        }else if(typeof area.nth !== "string"){
                            if(area.nth.full !== area.nth.count){
                                area.nth.count++
                            }
                        }
                    }
                }
                
            }
        }
        alert(`테스트 완료, F5를 누르면 다시 할 수 있습니다.`)
    }
    /*기능 추가로 실시간으로 학교별 count변수 상태 반영하는 막대 그래프? 배치하면 될 듯 $:잘 써서 실시간으로 반영 되도록 하면
    좀 긴장감도 있고 재밌을 것 같음*/
</script>
<h1>고등학교 원서 테스트기</h1>

<button on:click={()=>{
    let arr = []
    arr.push(schools.local["st"])
    arr.push(schools.local["nd"])
    arr.push(schools.local["rd"])
    arr.push(schools.local["th"])
    arr.push(schools.local["fth"])
    for(let i=0; i<5; i++){
        for(let j=i+1; j<5; j++){
            if(arr[i] === arr[j]){
                alert("지역내 배정에 중복된 학교가 있습니다. 수정해 주세요.")
                return
            }
        }
    }
    let brr = []
    brr.push(schools.area["st"])
    brr.push(schools.area["nd"])
    brr.push(schools.area["rd"])
    brr.push(schools.area["th"])
    brr.push(schools.area["fth"])
    brr.push(schools.area["sth"])
    brr.push(schools.area["seth"])
    brr.push(schools.area["eth"])
    brr.push(schools.area["nth"])
    for(let i=0; i<5; i++){
        for(let j=i+1; j<5; j++){
            if(brr[i] === brr[j]){
                alert("학군내 배정에 중복된 학교가 있습니다. 수정해 주세요.")
                return
            }
        }
    }
    let school = prompt("출신 중학교를 입력해 주세요.")
    let classs = prompt("반을 입력해 주세요")
    let num = prompt("번호를 입력해 주세요")
    if(typeof school === "string"&&typeof classs === "string"){
        high.강서고.count = 0;
        high.경안고.count = 0;
        high.고잔고.count = 0;
        high.광덕고.count = 0;
        high.단원고.count = 0;
        high.대부고.count = 0;
        high.부곡고.count = 0;
        high.상록고.count = 0;
        high.선부고.count = 0;
        high.성안고.count = 0;
        high.성포고.count = 0;
        high.송호고.count = 0;
        high.신길고.count = 0;
        high.안산고.count = 0;
        high.양지고.count = 0;
        high.원곡고.count = 0;
        high.초지고.count = 0;
        pick(school,Number(classs),Number(num))
    }
    
}}>테스트해 보기</button>
<div class="tables">
    <table>
        <tr>
            <th class="sub_title" colspan="3">지역내 배정</th>
        </tr>
        <tr>
            <td>지망 순위</td>
            <td>지망 학교</td>
            <td>배정 여부</td>
        </tr>
        <tr>
            <td>1지망</td>
            <td class="school" on:click={()=>{
                let answer = prompt()
                if(answer !== null){
                    let arr = Object.entries(high)
                    let a
                    for(let i=0; i<arr.length; i++){
                        if(arr[i][1].name === answer){
                            a = arr[i][1]
                        }
                    }
                    if(typeof a !== "undefined")
                    schools.local.st = a
                }
            }}>{schools.local["st"].name}</td>
            <td>?</td>
        </tr>
        <tr>
            <td>2지망</td>
            <td class="school" on:click={()=>{
                let answer = prompt()
                if(answer !== null){
                    let arr = Object.entries(high)
                    let a
                    for(let i=0; i<arr.length; i++){
                        if(arr[i][1].name === answer){
                            a = arr[i][1]
                        }
                    }
                    if(typeof a !== "undefined")
                    schools.local.nd = a
                }
            }}>{schools.local["nd"].name}</td>
            <td>?</td>
        </tr>
        <tr>
            <td>3지망</td>
            <td class="school" on:click={()=>{
                let answer = prompt()
                if(answer !== null){
                    let arr = Object.entries(high)
                    let a
                    for(let i=0; i<arr.length; i++){
                        if(arr[i][1].name === answer){
                            a = arr[i][1]
                        }
                    }
                    if(typeof a !== "undefined")
                    schools.local.rd = a
                }
            }}>{schools.local["rd"].name}</td>
            <td>?</td>
        </tr>
        <tr>
            <td>4지망</td>
            <td class="school" on:click={()=>{
                let answer = prompt()
                if(answer !== null){
                    let arr = Object.entries(high)
                    let a
                    for(let i=0; i<arr.length; i++){
                        if(arr[i][1].name === answer){
                            a = arr[i][1]
                        }
                    }
                    if(typeof a !== "undefined")
                    schools.local.th = a
                }
            }}>{schools.local["th"].name}</td>
            <td>?</td>
        </tr>
        <tr>
            <td>5지망</td>
            <td class="school" on:click={()=>{
                let answer = prompt()
                if(answer !== null){
                    let arr = Object.entries(high)
                    let a
                    for(let i=0; i<arr.length; i++){
                        if(arr[i][1].name === answer){
                            a = arr[i][1]
                        }
                    }
                    if(typeof a !== "undefined")
                    schools.local.fth = a
                }
            }}>{schools.local["fth"].name}</td>
            <td>?</td>
        </tr>
        <tr>
            <td>-</td>
            <td>-</td>
            <td>-</td>
        </tr>
        <tr>
            <td>-</td>
            <td>-</td>
            <td>-</td>
        </tr>
        <tr>
            <td>-</td>
            <td>-</td>
            <td>-</td>
        </tr>
        <tr>
            <td>-</td>
            <td>-</td>
            <td>-</td>
        </tr>
    </table>
    <table>
        <tr>
            <th class="sub_title" colspan="3">학군내 배정</th>
        </tr>
        <tr>
            <td>지망 순위</td>
            <td>지망 학교</td>
            <td>배정 여부</td>
        </tr>
        <tr>
            <td>1지망</td>
            <td class="school" on:click={()=>{
                let answer = prompt()
                if(answer !== null){
                    let arr = Object.entries(high)
                    let a
                    for(let i=0; i<arr.length; i++){
                        if(arr[i][1].name === answer){
                            a = arr[i][1]
                        }
                    }
                    if(typeof a !== "undefined")
                    schools.area.st = a
                }
            }}>{schools.area["st"].name}</td>
            <td>?</td>
        </tr>
        <tr>
            <td>2지망</td>
            <td class="school" on:click={()=>{
                let answer = prompt()
                if(answer !== null){
                    let arr = Object.entries(high)
                    let a
                    for(let i=0; i<arr.length; i++){
                        if(arr[i][1].name === answer){
                            a = arr[i][1]
                        }
                    }
                    if(typeof a !== "undefined")
                    schools.area.nd = a
                }
            }}>{schools.area["nd"].name}</td>
            <td>?</td>
        </tr>
        <tr>
            <td>3지망</td>
            <td class="school" on:click={()=>{
                let answer = prompt()
                if(answer !== null){
                    let arr = Object.entries(high)
                    let a
                    for(let i=0; i<arr.length; i++){
                        if(arr[i][1].name === answer){
                            a = arr[i][1]
                        }
                    }
                    if(typeof a !== "undefined")
                    schools.area.rd = a
                }
            }}>{schools.area["rd"].name}</td>
            <td>?</td>
        </tr>
        <tr>
            <td>4지망</td>
            <td class="school" on:click={()=>{
                let answer = prompt()
                if(answer !== null){
                    let arr = Object.entries(high)
                    let a
                    for(let i=0; i<arr.length; i++){
                        if(arr[i][1].name === answer){
                            a = arr[i][1]
                        }
                    }
                    if(typeof a !== "undefined")
                    schools.area.th = a
                }
            }}>{schools.area["th"].name}</td>
            <td>?</td>
        </tr>
        <tr>
            <td>5지망</td>
            <td class="school" on:click={()=>{
                let answer = prompt()
                if(answer !== null){
                    let arr = Object.entries(high)
                    let a
                    for(let i=0; i<arr.length; i++){
                        if(arr[i][1].name === answer){
                            a = arr[i][1]
                        }
                    }
                    if(typeof a !== "undefined")
                    schools.area.fth = a
                }
            }}>{schools.area["fth"].name}</td>
            <td>?</td>
        </tr>
        <tr>
            <td>6지망</td>
            <td class="school" on:click={()=>{
                let answer = prompt()
                if(answer !== null){
                    let arr = Object.entries(high)
                    let a
                    for(let i=0; i<arr.length; i++){
                        if(arr[i][1].name === answer){
                            a = arr[i][1]
                        }
                    }
                    if(typeof a !== "undefined")
                    schools.area.sth = a
                }
            }}>{schools.area["sth"].name}</td>
            <td>?</td>
        </tr>
        <tr>
            <td>7지망</td>
            <td class="school" on:click={()=>{
                let answer = prompt()
                if(answer !== null){
                    let arr = Object.entries(high)
                    let a
                    for(let i=0; i<arr.length; i++){
                        if(arr[i][1].name === answer){
                            a = arr[i][1]
                        }
                    }
                    if(typeof a !== "undefined")
                    schools.area.seth = a
                }
            }}>{schools.area["seth"].name}</td>
            <td>?</td>
        </tr>
        <tr>
            <td>8지망</td>
            <td class="school" on:click={()=>{
                let answer = prompt()
                if(answer !== null){
                    let arr = Object.entries(high)
                    let a
                    for(let i=0; i<arr.length; i++){
                        if(arr[i][1].name === answer){
                            a = arr[i][1]
                        }
                    }
                    if(typeof a !== "undefined")
                    schools.area.eth = a
                }
            }}>{schools.area["eth"].name}</td>
            <td>?</td>
        </tr>
        <tr>
            <td>9지망</td>
            <td class="school" on:click={()=>{
                let answer = prompt()
                if(answer !== null){
                    let arr = Object.entries(high)
                    let a
                    for(let i=0; i<arr.length; i++){
                        if(arr[i][1].name === answer){
                            a = arr[i][1]
                        }
                    }
                    if(typeof a !== "undefined")
                    schools.area.nth = a
                }
            }}>{schools.area["nth"].name}</td>
            <td>?</td>
        </tr>
    </table>
</div>
<div class="caution">
    <h3>주의 사항</h3>
    <ol>
        <li>출신 중학교, 원서 지망 고등학교 작성 시 <strong>ㅇㅇ고, ㅇㅇ중</strong> 같이 작성해 주세요.</li>
        <li>반, 번호를 작성 시 <strong>숫자</strong>만 입력해 주세요.</li>
        <li>결과가 실제 결과와 다소 다를 수 있습니다.</li>
        <li>기능 추가, 버그 제보 및 건의 사항은 milkway1128@gmail.com으로 보내주세요.</li>
    </ol> 
</div>

<style>
    .tables {
        display: flex;
        width: 40vw
    }

    table {
        border-collapse: collapse;
    }
    td {
        border: 1px solid black;
        text-align: center;
    }
    th {
        border: 1px solid black;
    }
    .school {
        transition: 0.2s;
    }
    .school:hover {
        cursor: pointer;
        background-color: rgb(182, 255, 240);
        font-weight: bolder;
    }
    .caution {
        display: flex;
        flex-direction: column;
        justify-content: center;
        width: 40vw;
        margin-left: -25px
    }
    h3 {
        text-align: center; 
        text-decoration: underline;
        color: red;
    }
</style>
