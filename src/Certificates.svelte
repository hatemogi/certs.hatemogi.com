<script lang="ts">
    import Certificate from './Certificate.svelte';

    interface CertRecord {
        제목: string;
        일자: string;
        이미지: string;
        url: string;
        태그: Array<string>;
        설명: string;
    }

    // 240x186 283x240
    let 수료증들: Array<CertRecord> = [
        {
            제목: 'Functional Programming Principles in Scala',
            일자: '2019/12',
            이미지: 'functional-programming-principles.png',
            url: 'https://www.coursera.org/account/accomplishments/verify/G8484AJVKD38',
            태그: ["스칼라", "함수형", "coursera"],
            설명: `스칼라 언어로 함수형 프로그래밍의 원리를 알려주는 수업입니다. 
                   명령형 프로그래밍과는 접근하는 출발점이 달라서 인상적이었습니다. 프로그램 코드를 기준으로,
                   증명(!)을 시도하는 것도 놀라웠구요. 재귀 호출 훈련을 받을 수 있습니다.`
        }, {
            제목: 'Functional Program Design in Scala',
            일자: '2019/12',
            이미지: 'functional-program-design.png',
            url: 'https://www.coursera.org/account/accomplishments/verify/C46AZ4X9TD8H',
            태그: ["스칼라", "함수형", "coursera"],
            설명: `스칼라 언어로 함수형 프로그래밍을 조금더 깊이있게 다루는 수업입니다. for-comprehension도 
                   본격적으로 활용하고, 모나드에 대해서도 알려줍니다. 비록 아직도 모나드를 잘 모르겠지만,
                   어쨌건 pure와 flatMap이 가능한 무언가라고 여겨봅시다.`
        }, {
            제목: 'Big Data Analysis with Scala and Spark',
            일자: '2019/12',
            이미지: 'bigdata-analysis.png',
            url: 'https://www.coursera.org/account/accomplishments/verify/9ZYD74J2N5QB',
            태그: ["스칼라", "함수형", "Spark", "빅데이터", "coursera"],
            설명: `대용량 데이터 분석을 도와주는 아파치 스파크에 대한 수업입니다. 스파크를 다루는 기초부터
                   활용까지 상세하게 알려줍니다. RDD가 무엇인지, 어떻게 효과적으로 활용해야 하는지 알 수 있게 됩니다.`
        }, {
            제목: 'Kotlin for Java Developers',
            일자: '2019/03',
            이미지: 'kotlin-for-java-developers.png',
            url: 'https://www.coursera.org/account/accomplishments/verify/YW847W7GCM88',
            태그: ["코틀린", "coursera"],
            설명: `Kotlin언어를 개발한 JetBrain사에서 직접 만든 수업입니다. 자바 개발자를 대상으로 코틀린을 쉽게 
                   배울 수 있도록 친절하게 설명해줍니다. 안드로이드 개발의 표준언어로 채택되었기에 관심을 갖고 
                   공부해보았습니다. 자바와 1:1 대응 구현이 가능하면서 매우 편리한 문법 기능이 많이있어서 좋았습니다.`
        }, {
            제목: 'Programming Reactive Systems',
            일자: '2020/12',
            이미지: 'reactive-systems.png',
            url: 'https://courses.edx.org/certificates/2bb6c61caef64f27a35d3f47e086390f',
            태그: ["반응형", "함수형", "스칼라", "edX"],
            설명: `동시성 처리가 편리한 액터 모델(actor model)을 구현한 Akka를 써서,
                   반응형 프로그래밍을 하는 방법을 알려주는 수업입니다. 반응형 프로그래밍이나,
                   Akka를 써서 서비스 개발을 해보실 분들께 추천드리는 수업입니다.`
        }
    ];
</script>

<section class="hero is-info">
    <div class="hero-body">
        <div class="container">
            <h1 class="title">프로그래밍 수업 수료증 모음</h1>
            <h2 class="subtitle">재미있게 들었던 유익한 수업들을 소개합니다. </h2>
        </div>
    </div>
</section>

<section class="section">
    <div class="container">
        <article class="message">
            <div class="message-body">
                <p>
                    모범생 친구들 집에 놀러가보면, 벽에 폼나는 상장들이 걸려 있었습니다.
                    하지만 제게는 그런 장식품이 없었지요.
                    그 부러웠던 마음을 이제라도 달래려, 그간 받은 수료증이라도 이렇게 온라인에 걸어두렵니다. 
                </p>
                <p>
                    요새는 정말 좋은 수업을 방안에서 편하게 들을 수 있어 좋은 것 같습니다.
                    해외에 있는 대학의 수업도 우리집 내 방에서 편안하게 들을 수 있는 시대인 거죠. 
                </p>
                <p>
                    넷플릭스나 유튜브가 제 여가 시간을 대부분을 차지하고 있습니다.
                    그래도 가끔은 큰 맘 먹고 수업을 듣고 나면 보람찬데요, 
                    여기에 이렇게 장식해 두고 만족감을 증폭시켜보겠습니다.
                    스스로에게 또 다시 좋은 자극제가 되어, 더 열심히 공부하면 좋지 않겠나 싶어서 말이죠.
                </p>
            </div>
        </article>
        {#each 수료증들 as 수료증}
            <Certificate {...수료증}></Certificate>
        {/each}
    </div>
</section>

<style>
    div.message-body {
        font-family: 'Poor Story', cursive;
    }
    div {
        font-family: 'Noto Serif KR', serif;
    }    
</style>
