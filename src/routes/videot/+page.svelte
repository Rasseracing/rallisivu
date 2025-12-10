<script lang="ts">
    let currentIndex = 0;

    function slideVideos(direction: number) {
        const container = document.querySelector(".video-container");
        const videos = document.querySelectorAll(".video-container iframe");
        const totalVideos = videos.length;
        const videoWidth = videos[0].clientWidth + 20; // 20px margin

        currentIndex += direction;

        if (currentIndex < 0) {
            currentIndex = totalVideos - 1;
        } else if (currentIndex >= totalVideos) {
            currentIndex = 0;
        }
    }
</script>

<h1>videoita</h1>
<div class="kaadot">
    <div class="video-carousel">
        <button class="prev" onclick={(_) => slideVideos(-1)}>&#10094;</button>
        <div>
            <h2>kaadot</h2>
            <iframe
                width="560"
                height="315"
                src="https://www.youtube.com/embed/b26LWct5V5k?si=4RcGeazl8ROW_bkM"
                title="YouTube video player"
                frameborder="0"
                allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share"
                referrerpolicy="strict-origin-when-cross-origin"
                allowfullscreen
            ></iframe>

            <iframe
                width="560"
                height="315"
                src="https://www.youtube.com/embed/gW2U7DXYLXk?si=4gbE9h6LZ1Q8ad5K"
                title="YouTube video player"
                frameborder="0"
                allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share"
                referrerpolicy="strict-origin-when-cross-origin"
                allowfullscreen
            ></iframe>
            <iframe
                width="560"
                height="315"
                src="https://www.youtube.com/embed/9-tIWJMSss0?si=cEqWF_guWDAOCvoc"
                title="YouTube video player"
                frameborder="0"
                allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share"
                referrerpolicy="strict-origin-when-cross-origin"
                allowfullscreen
            ></iframe>
        </div>
        <button class="next" onclick={(_) => slideVideos(1)}>&#10095;</button>
    </div>
</div>

<style>
    .prev,
    .next {
        background-color: rgba(0, 0, 0, 0.5);
        color: white;
        border: none;
        padding: 10px;
        cursor: pointer;
        height: 50px;
    }

    .prev {
        left: 0;
    }

    .next {
        right: 0;
    }
    .video-carousel {
        display: flex;
        align-items: center;
    }
</style>
