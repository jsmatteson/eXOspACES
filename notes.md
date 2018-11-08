main image:
https://img.youtube.com/vi/{{ page.youtube }}/0.jpg
thumbs:
https://img.youtube.com/vi/{{ page.youtube }}/1.jpg
https://img.youtube.com/vi/{{ page.youtube }}/2.jpg
https://img.youtube.com/vi/{{ page.youtube }}/3.jpg

highquality, http://img.youtube.com/vi/<insert-youtube-video-id-here>/hqdefault.jpg 

md quality no black, https://img.youtube.com/vi/KXObIJnV1_w/mqdefault.jpg 

max, https://img.youtube.com/vi/KXObIJnV1_w/maxresdefault.jpg

http://promincproductions.com/blog/youtube-image-thumbnail-urls/
https://www.thewebtaylor.com/articles/how-to-get-a-youtube-videos-thumbnail-image-in-high-quality

psychophysical;pareidolia;synesthesia;interdisciplinary;cross-disciplinary;symmetry;line;texture;haptic;optic;neon;Kandinsky;color field;abstract;non-representational;non-objective;non-figurative;computer;internet;iGen;GenX;retro;vintage;80s;video;app;gestural;noir;contemporary;gameplay;recording;index;sublime;aesthetics;systems;permutations;Constructionism;third screen;technology;drones

theme idea: 
- https://github.com/wowthemesnet/template-pintereso-bootstrap-jekyll

light gallery, http://sachinchoolur.github.io/lightGallery/demos/videos.html


video modal:

<!-- story box -->
<div class="col-sm-6 stories d-flex justify-content-center align-items-center mb-3" id="story{{ story.id }}" >
    <div class="" type="button" data-toggle="modal" data-target="#modal{{ story.id }}">
        <img src="{{ '/assets/images/' | append: story.image | relative_url }}" alt="{{ story.county }} person" class="img-fluid" style="max-width: 400px;">
    </div>
</div>
<!-- story modal -->
<div class="modal fade" id="modal{{ story.id }}" tabindex="-1" role="dialog" aria-labelledby="modalTitle{{ story.id }}" aria-hidden="true">
    <div class="modal-dialog modal-dialog-centered modal-lg" role="document">
        <div class="modal-content">
            <div class="modal-header">
                <h5 class="modal-title" id="modalTitle{{ story.id }}">{{ story.county }}</h5>
                <button type="button" class="close" data-dismiss="modal" aria-label="Close">
                    <span aria-hidden="true">&times;</span>
                </button>
            </div>
            <div class="modal-body">
                {% if story.youtube %}
                <div class="embed-responsive embed-responsive-16by9">
                    <iframe class="embed-responsive-item" src="https://www.youtube.com/embed/{{ story.youtube }}?rel=0" allowfullscreen></iframe>
                    </div>
                {% else %}
                <img class="img-fluid" src="{{ '/assets/images/' | append: story.image | relative_url }}" alt="{{ story.county }} person">
                {% endif %}
                <p>{{ story.story }}</p>
            </div>
        </div>
    </div>
</div>


$(document).ready(function() {
        $("#lightgallery").lightGallery({
            selector: '.gallery-img',
            loadYoutubeThumbnail:true,
            youtubePlayerParams: {
                modestbranding: 1,
                showinfo: 0,
                rel: 0,
                controls: 0
            }
        }); 
    });