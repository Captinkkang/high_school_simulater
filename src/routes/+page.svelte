<script>
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
        "중앙중":{"class_num":9,"name":"중앙중","full":10,"1or2":1},
        "단원중":{"class_num":6,"name":"중앙중","full":10,"1or2":1},
        "양지중":{"class_num":11,"name":"중앙중","full":10,"1or2":1},
        "성안중":{"class_num":6,"name":"중앙중","full":10,"1or2":1},
        "초지중":{"class_num":6,"name":"중앙중","full":10,"1or2":1},
        "해양중":{"class_num":6,"name":"중앙중","full":10,"1or2":1},
        "송호중":{"class_num":7,"name":"중앙중","full":10,"1or2":1},
        "별망중":{"class_num":5,"name":"중앙중","full":10,"1or2":1},
        "석호중":{"class_num":3,"name":"중앙중","full":10,"1or2":1},
        "시곡중":{"class_num":10,"name":"중앙중","full":10,"1or2":1},
        "선부중":{"class_num":6,"name":"중앙중","full":10,"1or2":1},
        "상록중":{"class_num":6,"name":"중앙중","full":10,"1or2":1},
        "반월중":{"class_num":4,"name":"중앙중","full":10,"1or2":1},
        "이호중":{"class_num":9,"name":"중앙중","full":10,"1or2":1},
        "부곡중":{"class_num":5,"name":"중앙중","full":10,"1or2":1},
        "경수중":{"class_num":5,"name":"중앙중","full":10,"1or2":1},
        "광덕중":{"class_num":2,"name":"중앙중","full":10,"1or2":1},
        "성호중":{"class_num":8,"name":"중앙중","full":10,"1or2":1},
        "성포중":{"class_num":5,"name":"중앙중","full":10,"1or2":1},
        "본오중":{"class_num":9,"name":"중앙중","full":10,"1or2":1},
        "관산중":{"class_num":6,"name":"중앙중","full":10,"1or2":1},
        "대부중":{"class_num":1,"name":"중앙중","full":10,"1or2":1},
        "석수중":{"class_num":5,"name":"중앙중","full":10,"1or2":1},
        "신길중":{"class_num":8,"name":"중앙중","full":10,"1or2":1},
        "선일중":{"class_num":3,"name":"선일중","full":10,"1or2":1},
        "와동중":{"class_num":5,"name":"와동중","full":10,"1or2":1},
        "원곡중":{"class_num":11,"name":"원곡중","full":10,"1or2":1},
        "원일중":{"class_num":8,"name":"원일중","full":10,"1or2":1},
        "안산중":{"class_num":2,"name":"안산중","full":10,"1or2":1},
        "해솔중":{"class_num":9,"name":"해솔중","full":10,"1or2":1},
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
