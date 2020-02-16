<template>
    <div class="Homepage">
        <section class="Homepage_heading bg-candy">
            <div class="Wrapper">
                <div class="row row-no-gutters">
                    <div class="col-6 pv-150">
                        <h1 class="ft-2xl">
                            <span class="color-sugar ft-xl">✌️ <b>antiswipe c'est</b></span><br> 
                            <b>des sorties sur Paris entre jeunes lgbt+ qui en ont <b>marre des applis de rencontres.</b></b>
                        </h1>
                    </div>
                    <div class="col-6 p-relative">
                        <div class="Homepage_gallery row row-no-gutters">
                            <div class="Homepage_galleryRow col-4" v-for="(rows, i) in polaroidRows" :key="i">
                                <polaroid-single
                                    v-for="item in rows.items"
                                    :title="item.title"
                                    :image="item.image"
                                    :key="item.id"
                                />
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </section>
    </div>
</template>

<script>
import polaroidSingle from '../components/polaroid-single'

export default {
    name: 'Homepage',
    components: { polaroidSingle },
    data: () => {
        return {
            headingGallery: [
                { id: 0, title: "Le brunch des lève-tôt", image: "" },
                { id: 0, title: "Pause #1", image: "" },
                { id: 0, title: "Welcome party #3", image: "" },
                { id: 0, title: "Killer party de la St-Valentin", image: "" },
                { id: 0, title: "Secret Santa", image: "" },
                { id: 0, title: "Welcome party #4", image: "" },
                { id: 0, title: "La nuit des gaymers", image: "" },
                { id: 0, title: "Meet & play #3", image: "" },
                { id: 0, title: "L'afterwork #2", image: "" },
                { id: 0, title: "Meet & play #2", image: "" },
                { id: 0, title: "Le musée du chocolat", image: "" }
            ]
        }
    },
    computed: {
        polaroidRows () {
            let rows = this.$data.headingGallery

            return [
                { items: rows }, { items: rows }, { items: rows }
            ]
        }
    }
}
</script>

<style lang="scss" scoped>
    .Homepage_heading {
        overflow: hidden;
    }

    .Homepage_gallery {
        position: absolute;
        left: 0;
        top: 40px;
        width: 700px;
        transform-origin: top;
        transform: rotate(3deg);
    }

    .Homepage_galleryRow {

        &:first-child {
            margin-top: 40px;
            transform: translateX(4px);
        }

        &:last-child {
            margin-top: 100px;
            transform: translateX(-4px);
        }
    }
</style>