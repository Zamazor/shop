<template>
<main>
              <nav class="navbar navbar-expand-lg navbar-dark" style="background: #32CD32;">
                <a class="navbar-brand" href="#" style="color: white;">Bycorp</a>
                        <div class="collapse navbar-collapse" id="navbarSupportedContent">
                            <ul class="navbar-nav mr-auto">
                                <li class="nav-item active">
                                    <NuxtLink to="/hom" class="text-white cd-md-3">
                                        Home
                                    </NuxtLink>
                                </li>
                                <li class="nav-item active">
                                    <NuxtLink to="/product" class="text-white col-md-3">
                                        Product
                                    </NuxtLink>
                                </li>
                                <li class="nav-item active">
                                    <NuxtLink to="/contact" class="text-white col-md-3">
                                        Contact
                                    </NuxtLink>
                                </li>
                            </ul>
                        </div>
            </nav>
  <div class="container">
    <div class="row">
      <div class="col-md-12">
       

        <div class="row">
          <div class="col-md-4" v-for="item in items" :key="item.id">
            <div class="card mb-3">
              <div class="card-header">
                <img :src="item.foto" width="100%">
              </div>
              <div class="card-body">
                <h4>{{ item.nama }}</h4>
                <h4>Rp{{ item.harga }}</h4>
                <a :href="item.link_eksternal" class="btn btn-success btn-block"> Meli Atuh AHHHH!!!</a>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
    <Footer />
  </div>
  </main>
</template>

<script>
export default {
  data() {
    return {
      items: "",
    };
  },
  mounted() {
    this.ambilData();
    },
    methods: {
      async ambilData() {
        const { data, error } = await this.$supabase.from("tbl_produk").select();
        if (data) this.items = data;
        if (error) console.log(error);
      },
    },
  };

</script>

