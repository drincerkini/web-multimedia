<template>
  <!-- Testimonial 3 - Bootstrap Brain Component -->
<section class="bg-light py-5 py-xl-8">

  <div class="container mb-5 mb-md-6 mb-xl-10">
    <div class="row justify-content-md-center">
      <div class="col-12 col-md-10 col-lg-8 col-xl-7 text-center">
        <h3 class="fs-6 text-secondary mb-2 text-uppercase"> {{ title }} </h3>
        <h2 class="display-5 mb-4 mb-md-5"> {{ desc }} </h2>
        <hr class="w-50 mx-auto mb-0 text-secondary">
      </div>
    </div>
  </div>

  <div class="container overflow-hidden">
    <div class="row gy-4 gy-md-0 gx-xxl-5"> 

      <!-- iteration through reviews array -->
      <div class="col-12 col-md-4" v-for="review in this.reviews" :key="review.name">
        <div class="card border-0 border-bottom border-primary shadow-sm">
          <div class="card-body p-4 p-xxl-5">
            <figure>
              <img class="img-fluid rounded rounded-circle mb-4 border border-5" loading="lazy" :src=review.img alt="">
              <figcaption>
                <div class="bsb-ratings text-warning mb-3" data-bsb-star="5" data-bsb-star-off="0"></div>
                <blockquote class="bsb-blockquote-icon mb-4">" {{ review.message }} "</blockquote>
                <h4 class="mb-2"> {{ review.name }} </h4>
                <h5 class="fs-6 text-secondary mb-0"> {{ review.position }} </h5>
              </figcaption>
            </figure>
          </div>
        </div>
        <!-- end of iteration -->

      </div>
    </div>
  </div>
</section>

</template>

<script>
import people1 from '../../assets/pppl1.jpg'
import people2 from '../../assets/ppl2.jpeg'
import people3 from '../../assets/ppl3.jpeg'

export default {
  data() {
    return {
      title: 'Happy Customers',
      desc: 'We deliver what we promise. See what clients are expressing about us.',

      reviews: [
        {
          img: people1,
          message: 'My recent stay at this hotel was exceptional! The staff was incredibly welcoming and attentive, ensuring that every aspect of my visit was perfect. The rooms were beautifully designed, offering stunning views of the city skyline.I highly recommend this hotel for a luxurious and memorable experience.',
          name: 'Luna John',
          position: 'UX Designer'
        },
        {
          img: people2,
          message: 'I had a fantastic time at this hotel during my vacation. The location was ideal, with easy access to nearby attractions and transportation. The staff went above and beyond to accommodate my requests and provided excellent recommendations for local dining options. I would definitely choose this hotel again for my next visit.',
          name: 'Mark Smith',
          position: 'Marketing Specialist'
        },
        {
          img: people3,
          message: 'My room was beautifully appointed, with luxurious amenities and a breathtaking view of the ocean. The on-site restaurant surpassed my expectations, serving delectable dishes with impeccable presentation. I cannot wait to return to this remarkable hotel.',
          name: 'Luke Reeves',
          position: 'Sales Manager'
        },
      ]
    }
  }
}

</script>