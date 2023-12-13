<script lang="ts">
    const schools = {
        "local":{"1st":"고잔고","2nd":"송호고","3rd":"성안고","4th":"양지고","5th":"경안고"},
        "area":{"1st":"고잔고","2nd":"경안고","3rd":"안산고","4th":"광덕고","5th":"송호고","6th":"성안고","7th":"부곡고","8th":"성포고","9th":"상록고"}
    }
    const high = {
        "고잔고":{"full":295,"name":"고잔고","count":0},
        "송호고":{"full":289,"name":"송호고","count":0},
        "경안고":{"full":312,"name":"경안고","count":0},
        "성안고":{"full":297,"name":"성안고","count":0},
        "상록고":{"full":301,"name":"상록고","count":0},
        "안산고":{"full":252,"name":"안산고","count":0},
        "성포고":{"full":280,"name":"성포고","count":0},
        "광덕고":{"full":237,"name":"광덕고","count":0},
        "양지고":{"full":251,"name":"양지고","count":0},
        "강서고":{"full":275,"name":"강서고","count":0},
        "선부고":{"full":235,"name":"선부고","count":0},
        "단원고":{"full":232,"name":"단원고","count":0},
        "부곡고":{"full":277,"name":"부곡고","count":0},
        "초지고":{"full":233,"name":"초지고","count":0},
        "대부고":{"full":15,"name":"대부고","count":0},
        "신길고":{"full":250,"name":"신길고","count":0},
        "원곡고":{"full":289,"name":"원곡고","count":0},
    }
    const middle = {
        "중앙중":{"class_num":9,"name":"중앙중","full":10,"1or2":1,"schools": {"local":{"1st":"경안고"},"area":{}}},
        "단원중":{"class_num":6,"name":"단원중","full":10,"1or2":1},
        "양지중":{"class_num":11,"name":"양지중","full":10,"1or2":1},
        "성안중":{"class_num":6,"name":"성안중","full":10,"1or2":1},
        "초지중":{"class_num":6,"name":"초지중","full":10,"1or2":1},
        "해양중":{"class_num":6,"name":"해양중","full":10,"1or2":1},
        "송호중":{"class_num":7,"name":"송호중","full":10,"1or2":1},
        "별망중":{"class_num":5,"name":"별망중","full":10,"1or2":1},
        "석호중":{"class_num":3,"name":"석호중","full":10,"1or2":1},
        "시곡중":{"class_num":10,"name":"시곡중","full":10,"1or2":1},
        "선부중":{"class_num":6,"name":"선부중","full":10,"1or2":1},
        "상록중":{"class_num":6,"name":"상록중","full":10,"1or2":1},
        "반월중":{"class_num":4,"name":"반월중","full":10,"1or2":1},
        "이호중":{"class_num":9,"name":"이호중","full":10,"1or2":1},
        "부곡중":{"class_num":5,"name":"부곡중","full":10,"1or2":1},
        "경수중":{"class_num":5,"name":"경수중","full":10,"1or2":1},
        "광덕중":{"class_num":2,"name":"광덕중","full":10,"1or2":1},
        "성호중":{"class_num":8,"name":"성호중","full":10,"1or2":1},
        "성포중":{"class_num":5,"name":"성포중","full":10,"1or2":1},
        "본오중":{"class_num":9,"name":"본오중","full":10,"1or2":1},
        "관산중":{"class_num":6,"name":"관산중","full":10,"1or2":1},
        "대부중":{"class_num":1,"name":"대부중","full":10,"1or2":1},
        "석수중":{"class_num":5,"name":"석수중","full":10,"1or2":1},
        "신길중":{"class_num":8,"name":"신길중","full":10,"1or2":1},
        "선일중":{"class_num":3,"name":"선일중","full":10,"1or2":1},
        "와동중":{"class_num":5,"name":"와동중","full":10,"1or2":1},
        "원곡중":{"class_num":11,"name":"원곡중","full":10,"1or2":1},
        "원일중":{"class_num":8,"name":"원일중","full":10,"1or2":1},
        "안산중":{"class_num":2,"name":"안산중","full":10,"1or2":1},
        "해솔중":{"class_num":9,"name":"해솔중","full":10,"1or2":1},
    }
    
    const pick = (school:string,room:string,id:number) => {
        let arr = Object.entries(middle)
        let aarr=[]
        let school_turn = []
        for(let i=0; i<arr.length; i++){
            aarr.push(arr[i][0])
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
        for(let i=1; i<=school_turn.length; i++){
            if(school_turn[i] === school)alert(`당신의 학교는 ${i}번째 입니다.`)
        }
        for(let i=1; i<=room_turn.length; i++){
            if(room_turn[i] === Number(room))alert(`당신의 학급은 ${i}번째 입니다.`)
        }
        for(let i=1; i<=id_turn.length; i++){
            if(id_turn[i] === id)alert(`당신의 순서는 ${i}번째 입니다.`)
        }

        /*학교별로 기준이 되는 원서를 정해서 그 원서에 맞게 정한다.
        학생을 배열?로 저장한 뒤 자기 학교에 자기반, 자기 번호에 있는 학생에는 me라느 변수를 대신 push하고
        자기 차례가 되면 남는 자리에 안착 후 결과에 따라 여부칸을 빨간색, 초록색으로 표시
        high객체의 각각의 내부 객체에 있는 count와 full이 같으면 더이상 그 학교는 들어갈 수 없다
        만약 자신이 아무데에도 당첨되지 못했다면 자신이 작성한 schools 객체에 없는 다른 자리가 남는 학교중 랜덤으로 간다
        */
    }
</script>
<h1>고등학교 원서 테스트기</h1>

<button on:click={()=>{
    let arr = []
    arr.push(schools.local["1st"])
    arr.push(schools.local["2nd"])
    arr.push(schools.local["3rd"])
    arr.push(schools.local["4th"])
    arr.push(schools.local["5th"])
    for(let i=0; i<5; i++){
        for(let j=i+1; j<5; j++){
            if(arr[i] === arr[j]){
                alert("지역내 배정에 중복된 학교가 있습니다. 수정해 주세요.")
                return
            }
        }
    }
    let brr = []
    brr.push(schools.area["1st"])
    brr.push(schools.area["2nd"])
    brr.push(schools.area["3rd"])
    brr.push(schools.area["4th"])
    brr.push(schools.area["5th"])
    brr.push(schools.area["6th"])
    brr.push(schools.area["7th"])
    brr.push(schools.area["8th"])
    brr.push(schools.area["9th"])
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
    if(typeof school === "string"&&typeof classs === "string")
    pick(school,classs,Number(num))
}}>테스트해 보기</button>
<div>
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
                if(answer !== null)
                schools.local["1st"] = answer
            }}>{schools.local["1st"]}</td>
            <td>?</td>
        </tr>
        <tr>
            <td>2지망</td>
            <td class="school" on:click={()=>{
                let answer = prompt()
                if(answer !== null)
                schools.local["2nd"] = answer
            }}>{schools.local["2nd"]}</td>
            <td>?</td>
        </tr>
        <tr>
            <td>3지망</td>
            <td class="school" on:click={()=>{
                let answer = prompt()
                if(answer !== null)
                schools.local["3rd"] = answer
            }}>{schools.local["3rd"]}</td>
            <td>?</td>
        </tr>
        <tr>
            <td>4지망</td>
            <td class="school" on:click={()=>{
                let answer = prompt()
                if(answer !== null)
                schools.local["4th"] = answer
            }}>{schools.local["4th"]}</td>
            <td>?</td>
        </tr>
        <tr>
            <td>5지망</td>
            <td class="school" on:click={()=>{
                let answer = prompt()
                if(answer !== null)
                schools.local["5th"] = answer
            }}>{schools.local["5th"]}</td>
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
                if(answer !== null)
                schools.area["1st"] = answer
            }}>{schools.area["1st"]}</td>
            <td>?</td>
        </tr>
        <tr>
            <td>2지망</td>
            <td class="school" on:click={()=>{
                let answer = prompt()
                if(answer !== null)
                schools.area["2nd"] = answer
            }}>{schools.area["2nd"]}</td>
            <td>?</td>
        </tr>
        <tr>
            <td>3지망</td>
            <td class="school" on:click={()=>{
                let answer = prompt()
                if(answer !== null)
                schools.area["3rd"] = answer
            }}>{schools.area["3rd"]}</td>
            <td>?</td>
        </tr>
        <tr>
            <td>4지망</td>
            <td class="school" on:click={()=>{
                let answer = prompt()
                if(answer !== null)
                schools.area["4th"] = answer
            }}>{schools.area["4th"]}</td>
            <td>?</td>
        </tr>
        <tr>
            <td>5지망</td>
            <td class="school" on:click={()=>{
                let answer = prompt()
                if(answer !== null)
                schools.area["5th"] = answer
            }}>{schools.area["5th"]}</td>
            <td>?</td>
        </tr>
        <tr>
            <td>6지망</td>
            <td class="school" on:click={()=>{
                let answer = prompt()
                if(answer !== null)
                schools.area["6th"] = answer
            }}>{schools.area["6th"]}</td>
            <td>?</td>
        </tr>
        <tr>
            <td>7지망</td>
            <td class="school" on:click={()=>{
                let answer = prompt()
                if(answer !== null)
                schools.area["7th"] = answer
            }}>{schools.area["7th"]}</td>
            <td>?</td>
        </tr>
        <tr>
            <td>8지망</td>
            <td class="school" on:click={()=>{
                let answer = prompt()
                if(answer !== null)
                schools.area["8th"] = answer
            }}>{schools.area["8th"]}</td>
            <td>?</td>
        </tr>
        <tr>
            <td>9지망</td>
            <td class="school" on:click={()=>{
                let answer = prompt()
                if(answer !== null)
                schools.area["9th"] = answer
            }}>{schools.area["9th"]}</td>
            <td>?</td>
        </tr>
    </table>
</div>

<style>
    div {
        display: flex;
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
</style>
