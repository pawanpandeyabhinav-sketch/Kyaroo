<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>Fashion Store - 299</title>

<style>
*{
    margin:0;
    padding:0;
    box-sizing:border-box;
    font-family:Arial,Helvetica,sans-serif;
}

body{
    background:#f6f6f6;
    color:#333;
}

/* ================= HEADER ================= */

.header{
    height:65px;
    background:#fff;
    border-bottom:1px solid #e5e5e5;
    display:flex;
    align-items:center;
    padding:0 7%;
    gap:35px;
    position:sticky;
    top:0;
    z-index:1000;
}

.logo{
    font-size:28px;
    font-weight:700;
    color:#f43397;
}

.search{
    height:42px;
    max-width:600px;
    flex:1;
    background:#f5f5f5;
    border:1px solid #ddd;
    border-radius:5px;
    display:flex;
    align-items:center;
    padding:0 15px;
    color:#777;
}

.header-right{
    display:flex;
    gap:25px;
    white-space:nowrap;
    font-size:14px;
}

/* ================= MAIN ================= */

.container{
    max-width:1200px;
    margin:25px auto;
    padding:0 15px;
}

.product-card{
    background:#fff;
    border-radius:5px;
    display:grid;
    grid-template-columns:55% 45%;
    overflow:hidden;
}

/* ================= GALLERY ================= */

.gallery{
    display:grid;
    grid-template-columns:85px 1fr;
    gap:18px;
    padding:25px;
}

.thumbnails{
    display:flex;
    flex-direction:column;
    gap:12px;
}

.thumbnail{
    width:72px;
    height:85px;
    border:1px solid #ddd;
    border-radius:5px;
    overflow:hidden;
    cursor:pointer;
    background:#fff;
}

.thumbnail.active{
    border:2px solid #f43397;
}

.thumbnail img{
    width:100%;
    height:100%;
    object-fit:cover;
}

.main-image{
    width:100%;
    height:520px;
    display:flex;
    align-items:center;
    justify-content:center;
    background:#fafafa;
    border-radius:5px;
    overflow:hidden;
}

.main-image img{
    width:100%;
    height:100%;
    object-fit:contain;
}

/* ================= DETAILS ================= */

.details{
    padding:35px 35px 35px 5px;
}

.title{
    font-size:23px;
    line-height:1.45;
    font-weight:500;
    margin-bottom:15px;
}

.rating-row{
    display:flex;
    align-items:center;
    gap:10px;
    margin-bottom:15px;
}

.rating{
    background:#038d63;
    color:#fff;
    padding:5px 9px;
    border-radius:4px;
    font-size:13px;
}

.reviews{
    color:#777;
    font-size:13px;
}

.price{
    font-size:32px;
    font-weight:700;
    margin-top:10px;
}

.mrp{
    color:#888;
    text-decoration:line-through;
    font-size:16px;
    font-weight:400;
    margin-left:8px;
}

.discount{
    color:#038d63;
    font-size:15px;
    font-weight:500;
    margin-left:8px;
}

.tax{
    color:#777;
    font-size:12px;
    margin-top:5px;
}

.divider{
    height:1px;
    background:#eee;
    margin:25px 0;
}

/* ================= SIZE ================= */

.section-title{
    font-size:16px;
    font-weight:600;
    margin-bottom:12px;
}

.sizes{
    display:flex;
    gap:10px;
}

.size{
    width:50px;
    height:40px;
    border:1px solid #aaa;
    border-radius:4px;
    display:flex;
    justify-content:center;
    align-items:center;
    cursor:pointer;
    background:#fff;
}

.size:hover,
.size.selected{
    border:2px solid #f43397;
    color:#f43397;
}

/* ================= QUANTITY ================= */

.quantity-section{
    margin-top:22px;
}

.quantity-box{
    display:flex;
    width:max-content;
    border:1px solid #ccc;
    border-radius:4px;
    overflow:hidden;
}

.quantity-box button{
    width:38px;
    height:38px;
    border:0;
    background:#fff;
    font-size:20px;
    cursor:pointer;
}

.quantity-number{
    width:42px;
    height:38px;
    display:flex;
    justify-content:center;
    align-items:center;
    border-left:1px solid #ddd;
    border-right:1px solid #ddd;
}

/* ================= BUTTONS ================= */

.buttons{
    display:flex;
    gap:12px;
    margin-top:28px;
}

.button{
    flex:1;
    height:52px;
    border-radius:5px;
    font-size:16px;
    font-weight:600;
    cursor:pointer;
}

.add-cart{
    background:#fff;
    color:#f43397;
    border:1px solid #f43397;
}

.buy-now{
    background:#f43397;
    color:#fff;
    border:1px solid #f43397;
}

.button:hover{
    opacity:.9;
}

/* ================= DELIVERY ================= */

.delivery{
    margin-top:25px;
}

.pincode-box{
    display:flex;
    margin-top:12px;
    max-width:390px;
}

.pincode-box input{
    height:45px;
    flex:1;
    border:1px solid #ccc;
    border-radius:4px 0 0 4px;
    padding:0 12px;
    outline:none;
}

.check-btn{
    width:90px;
    border:1px solid #f43397;
    background:#fff;
    color:#f43397;
    font-weight:600;
    border-radius:0 4px 4px 0;
    cursor:pointer;
}

/* ================= BENEFITS ================= */

.benefits{
    display:grid;
    grid-template-columns:repeat(3,1fr);
    gap:8px;
    margin-top:25px;
}

.benefit{
    background:#fafafa;
    border-radius:4px;
    padding:15px 5px;
    text-align:center;
    font-size:12px;
    color:#555;
}

.benefit-icon{
    font-size:22px;
    margin-bottom:5px;
}

/* ================= DESCRIPTION ================= */

.description{
    background:#fff;
    margin-top:18px;
    padding:25px;
    border-radius:5px;
}

.description h2{
    font-size:20px;
    margin-bottom:18px;
}

.description p{
    color:#666;
    line-height:1.7;
    font-size:14px;
}

.details-table{
    margin-top:18px;
    width:100%;
    max-width:600px;
    border-collapse:collapse;
}

.details-table td{
    padding:10px;
    border-bottom:1px solid #eee;
    font-size:14px;
}

.details-table td:first-child{
    color:#777;
    width:40%;
}

/* ================= TOAST ================= */

.toast{
    position:fixed;
    bottom:25px;
    right:25px;
    background:#222;
    color:white;
    padding:14px 20px;
    border-radius:5px;
    display:none;
    z-index:2000;
}

/* ================= MOBILE ================= */

@media(max-width:800px){

    .header{
        padding:0 15px;
        gap:15px;
    }

    .logo{
        font-size:24px;
    }

    .search{
        display:none;
    }

    .header-right{
        margin-left:auto;
        gap:12px;
        font-size:12px;
    }

    .product-card{
        grid-template-columns:1fr;
    }

    .gallery{
        grid-template-columns:62px 1fr;
        padding:12px;
        gap:10px;
    }

    .thumbnail{
        width:57px;
        height:70px;
    }

    .main-image{
        height:390px;
    }

    .details{
        padding:20px;
    }

    .title{
        font-size:19px;
    }

    .price{
        font-size:28px;
    }

    .benefits{
        grid-template-columns:repeat(3,1fr);
    }

    .buttons{
        position:sticky;
        bottom:0;
        background:white;
        padding:10px 0;
        z-index:20;
    }
}

@media(max-width:450px){

    .header-right span:first-child{
        display:none;
    }

    .main-image{
        height:330px;
    }

    .benefit{
        font-size:10px;
    }

    .button{
        font-size:14px;
    }
}
</style>
</head>


<body>

<!-- ================= HEADER ================= -->

<header class="header">

    <div class="logo">
        kyora
    </div>

    <div class="search">
         &nbsp; Search for products, brands and more
    </div>

    <div class="header-right">
        <span>Become a Supplier</span>
        <span> Cart</span>
    </div>

</header>


<main class="container">

    <!-- ================= PRODUCT ================= -->

    <section class="product-card">

        <!-- IMAGE GALLERY -->

        <div class="gallery">

            <div class="thumbnails">

                <div
                    class="thumbnail active"
                    onclick="changeImage(0)"
                >
                    <img
                        src="https://plain-apac-prod-public.komododecks.com/202609/26/3XHfjiauI0hrJQdp5Ml2/image.jpg"
                        alt="Product image 1"
                    >
                </div>


                <div
                    class="thumbnail"
                    onclick="changeImage(1)"
                >
                    <img
                        src="https://plain-apac-prod-public.komododecks.com/202609/26/AIS2ik8csYaavBmuwVbC/image.jpg"
                        alt="Product image 2"
                    >
                </div>

            </div>


            <div class="main-image">

                <img
                    id="mainProduct"
                    src="https://plain-apac-prod-public.komododecks.com/202609/26/3XHfjiauI0hrJQdp5Ml2/image.jpg"
                    alt="Men's T-shirt combo"
                >

            </div>

        </div>


        <!-- PRODUCT DETAILS -->

        <div class="details">

            <h1 class="title">
                Men's Stylish Cotton T-Shirt Combo
            </h1>


            <div class="rating-row">

                <span class="rating">
                     4.2
                </span>

                <span class="reviews">
                    1,245 Ratings & Reviews
                </span>

            </div>


            <div class="price">

                299

                <span class="mrp">
                    699
                </span>

                <span class="discount">
                    57% OFF
                </span>

            </div>

            <div class="tax">
                Inclusive of all taxes
            </div>


            <div class="divider"></div>


            <!-- SIZE -->

            <div class="section-title">
                Select Size
            </div>

            <div class="sizes">

                <div class="size" onclick="selectSize(this)">
                    S
                </div>

                <div class="size selected" onclick="selectSize(this)">
                    M
                </div>

                <div class="size" onclick="selectSize(this)">
                    L
                </div>

                <div class="size" onclick="selectSize(this)">
                    XL
                </div>

                <div class="size" onclick="selectSize(this)">
                    XXL
                </div>

            </div>


            <!-- QUANTITY -->

            <div class="quantity-section">

                <div class="section-title">
                    Quantity
                </div>

                <div class="quantity-box">

                    <button onclick="decreaseQuantity()">
                        
                    </button>

                    <div
                        class="quantity-number"
                        id="quantity"
                    >
                        1
                    </div>

                    <button onclick="increaseQuantity()">
                        +
                    </button>

                </div>

            </div>


            <!-- BUTTONS -->

            <div class="buttons">

                <button
                    class="button add-cart"
                    onclick="addToCart()"
                >
                     Add to Cart
                </button>

                <button
                    class="button buy-now"
                    onclick="buyNow()"
                >
                    Buy Now
                </button>

            </div>


            <!-- DELIVERY -->

            <div class="delivery">

                <div class="section-title">
                     Delivery Details
                </div>

                <div class="pincode-box">

                    <input
                        id="pincode"
                        type="text"
                        maxlength="6"
                        placeholder="Enter Pincode"
                    >

                    <button
                        class="check-btn"
                        onclick="checkPincode()"
                    >
                        Check
                    </button>

                </div>

            </div>


            <!-- BENEFITS -->

            <div class="benefits">

                <div class="benefit">

                    <div class="benefit-icon">
                        
                    </div>

                    Free Delivery

                </div>


                <div class="benefit">

                    <div class="benefit-icon">
                        
                    </div>

                    Easy Returns

                </div>


                <div class="benefit">

                    <div class="benefit-icon">
                        
                    </div>

                    Secure Payment

                </div>

            </div>

        </div>

    </section>


    <!-- ================= DESCRIPTION ================= -->

    <section class="description">

        <h2>
            Product Details
        </h2>

        <p>
            Upgrade your everyday wardrobe with this stylish
            men's cotton T-shirt collection. Designed for
            comfortable everyday wear with a casual modern look.
        </p>


        <table class="details-table">

            <tr>
                <td>Product Type</td>
                <td>Men's T-Shirt</td>
            </tr>

            <tr>
                <td>Fabric</td>
                <td>Cotton</td>
            </tr>

            <tr>
                <td>Fit</td>
                <td>Regular Fit</td>
            </tr>

            <tr>
                <td>Occasion</td>
                <td>Casual Wear</td>
            </tr>

            <tr>
                <td>Sizes</td>
                <td>S, M, L, XL, XXL</td>
            </tr>

            <tr>
                <td>Price</td>
                <td>299</td>
            </tr>

        </table>

    </section>

</main>


<!-- TOAST -->

<div
    class="toast"
    id="toast"
>
    Added to cart 
</div>


<script>

/* ================= IMAGES ================= */

const productImages = [

    "https://plain-apac-prod-public.komododecks.com/202609/26/3XHfjiauI0hrJQdp5Ml2/image.jpg",

    "https://plain-apac-prod-public.komododecks.com/202609/26/AIS2ik8csYaavBmuwVbC/image.jpg"

];


/* ================= IMAGE SWITCH ================= */

function changeImage(index){

    document.getElementById("mainProduct").src =
        productImages[index];

    const thumbnails =
        document.querySelectorAll(".thumbnail");

    thumbnails.forEach((thumbnail, i) => {

        thumbnail.classList.toggle(
            "active",
            i === index
        );

    });

}


/* ================= SIZE ================= */

function selectSize(element){

    document
        .querySelectorAll(".size")
        .forEach(size => {

            size.classList.remove("selected");

        });

    element.classList.add("selected");

}


/* ================= QUANTITY ================= */

let quantity = 1;


function increaseQuantity(){

    quantity++;

    document.getElementById("quantity").innerText =
        quantity;

}


function decreaseQuantity(){

    if(quantity > 1){

        quantity--;

        document.getElementById("quantity").innerText =
            quantity;

    }

}


/* ================= CART ================= */

function addToCart(){

    showToast(
        "Product added to cart "
    );

}


/* ================= BUY ================= */

function buyNow(){

    const selectedSize =
        document.querySelector(".size.selected").innerText;

    const total =
        299 * quantity;

    showToast(
        "Order: Size " +
        selectedSize +
        " � " +
        quantity +
        " = " +
        total
    );

}


/* ================= PINCODE ================= */

function checkPincode(){

    const pincode =
        document.getElementById("pincode").value.trim();

    if(pincode.length !== 6){

        showToast(
            "Please enter a valid 6-digit pincode"
        );

        return;

    }

    showToast(
        "Delivery available "
    );

}


/* ================= TOAST ================= */

function showToast(message){

    const toast =
        document.getElementById("toast");

    toast.innerText =
        message;

    toast.style.display =
        "block";

    setTimeout(() => {

        toast.style.display =
            "none";

    }, 2500);

}

</script>

</body>
</html>
