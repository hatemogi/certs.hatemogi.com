<script lang="ts">
    // 코스제목 수료증썸네일 수료증url 내용 태그 언제
    export let 제목: string = ''
    export let 일자: string = ''
    export let 이미지: string = ''
    export let url: string = ''
    export let 태그: Array<string> = []
    export let 설명: string = ''
</script>

<div class="box">
    <article class="media">
        <div class="media-left">
            <figure class="image">
                <a href={url}>
                    <img src="thumbnails/{이미지}" alt="수료증이미지" srcset="thumbnails/{이미지} 2x"/>
                </a>
            </figure>    
        </div>
        <div class="media-content">
            <div class="content">
                <h3><a href={url}>{제목}</a><small class="is-pulled-right">{일자}</small></h3>
                <p>{설명}</p>
            </div>
            <div class="tags">
                {#each 태그 as tag}
                <span class="tag is-info">{tag}</span>
                {/each}
            </div>
        </div>
    </article>
</div>

<style>
    h3 {
        font-family: 'Great Vibes', cursive;
    }
    img:hover {
        animation: 1s;
        transform: scale(1.2); 
    }
    span.tag {
        font-family: sans-serif;
    }
</style>
