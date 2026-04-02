<!DOCTYPE html>
<html lang="es">
<head>
<meta charset="UTF-8"><meta name="viewport" content="width=device-width,initial-scale=1">
<title>Aynigames — Catálogo Profesional de Juegos de Mesa</title>
<meta name="description" content="Los mejores juegos de mesa en Bolivia. Cartas, tablero y estrategia. Envíos a todo el país.">
<link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700;800&family=Playfair+Display:ital,wght@0,700;0,800;1,700&display=swap" rel="stylesheet">
<style>
/* ===== ESTILOS COMPLETOS (mismos que la versión profesional Aynigames) ===== */
:root{--w:#7B1E2E;--wd:#4F1320;--wl:#9C2840;--g:#D4A843;--gl:#F0C96A;--bg:#F6F4F1;--card:#fff;--txt:#1C1C1E;--mid:#4A4A55;--soft:#8A8A9A;--brd:#E5E2DD;--r:16px;--rs:10px;--e:cubic-bezier(.4,0,.2,1)}
*{margin:0;padding:0;box-sizing:border-box}html{scroll-behavior:smooth}
body{font-family:'Inter',sans-serif;background:var(--bg);color:var(--txt);min-height:100vh}
button{font-family:'Inter',sans-serif;cursor:pointer}a{text-decoration:none;color:inherit}
::-webkit-scrollbar{width:5px}::-webkit-scrollbar-thumb{background:var(--w);border-radius:3px}

/* TOP BAR */
.topbar{background:var(--wd);color:rgba(255,255,255,.82);text-align:center;padding:.4rem 1rem;font-size:.76rem;font-weight:500;letter-spacing:.4px}
.topbar strong{color:var(--gl)}

/* HEADER */
header{background:rgba(255,255,255,.88);backdrop-filter:blur(20px);border-bottom:1px solid rgba(229,226,221,.6);position:sticky;top:0;z-index:400;transition:box-shadow .3s var(--e)}
header.scrolled{box-shadow:0 4px 24px rgba(0,0,0,.09)}
.hdr{max-width:1360px;margin:0 auto;padding:.85rem 2rem;display:flex;align-items:center;gap:1.4rem;flex-wrap:wrap}
.logo{display:flex;align-items:center;gap:.7rem;flex-shrink:0}
.logo-ico{width:46px;height:46px;background:linear-gradient(135deg,var(--w),var(--wd));border-radius:12px;display:flex;align-items:center;justify-content:center;box-shadow:0 4px 14px rgba(123,30,46,.28)}
.logo-ico svg{width:24px;height:24px;fill:none;stroke:#fff;stroke-width:1.8}
.logo-t{display:flex;flex-direction:column;line-height:1.1}
.logo-name{font-family:'Playfair Display',serif;font-size:1.45rem;font-weight:800;color:var(--w);letter-spacing:-.4px}
.logo-sub{font-size:.63rem;color:var(--soft);letter-spacing:2px;text-transform:uppercase;font-weight:600}
.srch{flex:1;max-width:420px;position:relative}
.srch svg{position:absolute;left:13px;top:50%;transform:translateY(-50%);width:16px;height:16px;stroke:var(--soft);stroke-width:2;fill:none;pointer-events:none}
.srch input{width:100%;padding:.68rem 1rem .68rem 2.6rem;border:1.5px solid var(--brd);border-radius:50px;font-size:.9rem;font-family:'Inter',sans-serif;background:#faf9f7;color:var(--txt);transition:all .25s var(--e)}
.srch input:focus{outline:none;border-color:var(--w);background:#fff;box-shadow:0 0 0 4px rgba(123,30,46,.08)}
nav.links{display:flex;gap:.1rem}
.nl{padding:.48rem .9rem;border-radius:var(--rs);font-size:.86rem;font-weight:600;color:var(--mid);transition:all .2s var(--e)}
.nl:hover{background:rgba(123,30,46,.06);color:var(--w)}
.cart-b{display:flex;align-items:center;gap:.45rem;background:linear-gradient(135deg,var(--w),var(--wd));color:#fff;border:none;padding:.62rem 1.3rem;border-radius:50px;font-weight:700;font-size:.86rem;box-shadow:0 4px 14px rgba(123,30,46,.3);transition:all .25s var(--e);flex-shrink:0}
.cart-b:hover{transform:translateY(-2px);box-shadow:0 8px 20px rgba(123,30,46,.42)}
.cart-b svg{width:17px;height:17px;stroke:#fff;stroke-width:2;fill:none}
.cbadge{background:var(--g);color:var(--wd);border-radius:50%;width:19px;height:19px;display:flex;align-items:center;justify-content:center;font-size:.68rem;font-weight:800}
@keyframes pop{0%,100%{transform:scale(1)}50%{transform:scale(1.15)}}
.cart-b.pop{animation:pop .38s var(--e)}

/* SLIDER */
.slider{position:relative;width:100%;height:90vh;min-height:500px;max-height:750px;overflow:hidden}
.slides{display:flex;height:100%;transition:transform .7s cubic-bezier(.77,0,.18,1)}
.slide{min-width:100%;height:100%;position:relative;display:flex;align-items:center;overflow:hidden}
.slide-bg{position:absolute;inset:0;background-size:cover !important;background-position:center !important;transition:transform 8s linear}
.slide-overlay{position:absolute;inset:0;background:linear-gradient(120deg,rgba(10,2,6,.88) 0%,rgba(10,2,6,.55) 55%,transparent 100%)}
.slide-content{position:relative;z-index:2;max-width:1360px;margin:0 auto;padding:0 2rem;width:100%}
.slide-tag{display:inline-flex;align-items:center;gap:.4rem;background:rgba(212,168,67,.2);border:1px solid rgba(212,168,67,.4);color:var(--gl);padding:.32rem 1rem;border-radius:50px;font-size:.74rem;font-weight:700;text-transform:uppercase;margin-bottom:1.2rem;opacity:0;transform:translateY(20px);transition:all .6s .2s var(--e)}
.slide.active .slide-tag{opacity:1;transform:none}
.slide h2{font-family:'Playfair Display',serif;font-size:clamp(2rem,5vw,3.8rem);color:#fff;line-height:1.1;margin-bottom:1rem;opacity:0;transform:translateY(30px);transition:all .6s .35s var(--e)}
.slide.active h2{opacity:1;transform:none}
.slide h2 em{font-style:italic;color:var(--gl)}
.slide p{font-size:1.05rem;color:rgba(255,255,255,.78);line-height:1.75;max-width:500px;margin-bottom:2rem;opacity:0;transform:translateY(20px);transition:all .6s .5s var(--e)}
.slide.active p{opacity:1;transform:none}
.slide-btns{display:flex;gap:1rem;flex-wrap:wrap;opacity:0;transform:translateY(20px);transition:all .6s .65s var(--e)}
.slide.active .slide-btns{opacity:1;transform:none}
.sl-dots{position:absolute;bottom:1.5rem;left:50%;transform:translateX(-50%);display:flex;gap:.5rem;z-index:10}
.sl-dot{width:8px;height:8px;border-radius:50%;background:rgba(255,255,255,.35);border:none;cursor:pointer;transition:all .3s var(--e)}
.sl-dot.on{background:var(--gl);width:24px;border-radius:4px}
.sl-arrow{position:absolute;top:50%;transform:translateY(-50%);z-index:10;background:rgba(255,255,255,.12);backdrop-filter:blur(8px);border:1px solid rgba(255,255,255,.2);color:#fff;width:46px;height:46px;border-radius:50%;display:flex;align-items:center;justify-content:center;cursor:pointer;transition:all .25s var(--e)}
.sl-arrow:hover{background:rgba(255,255,255,.25)}
.sl-arrow svg{width:20px;height:20px;stroke:#fff;stroke-width:2;fill:none}
.sl-prev{left:1.5rem}.sl-next{right:1.5rem}

/* TRUST BAR */
.trust{background:#fff;border-bottom:1px solid var(--brd)}
.trust-in{max-width:1360px;margin:0 auto;padding:1.1rem 2rem;display:flex;justify-content:center;gap:3rem;flex-wrap:wrap}
.ti{display:flex;align-items:center;gap:.65rem}
.ti-ico{width:36px;height:36px;background:rgba(123,30,46,.08);border-radius:9px;display:flex;align-items:center;justify-content:center}
.ti-ico svg{width:18px;height:18px;stroke:var(--w);stroke-width:1.8;fill:none}
.ti strong{display:block;font-size:.82rem;font-weight:700;color:var(--txt)}
.ti span{font-size:.72rem;color:var(--soft)}

/* SECCIONES */
.sec-hdr{max-width:1360px;margin:0 auto;padding:2.8rem 2rem 1rem;display:flex;justify-content:space-between;align-items:flex-end;flex-wrap:wrap;gap:1rem}
.sec-h2{font-family:'Playfair Display',serif;font-size:1.7rem;font-weight:800;color:var(--txt);letter-spacing:-.3px}
.sec-h2 span{color:var(--w)}
.sec-sub{font-size:.83rem;color:var(--soft);margin-top:.25rem;font-weight:500}
.filters{max-width:1360px;margin:0 auto;padding:.5rem 2rem 0;display:flex;gap:.6rem;flex-wrap:wrap}
.chip{background:#fff;border:1.5px solid var(--brd);padding:.45rem 1.1rem;border-radius:50px;font-size:.82rem;font-weight:600;color:var(--mid);transition:all .22s var(--e);white-space:nowrap}
.chip:hover{border-color:var(--w);color:var(--w)}
.chip.on{background:var(--w);border-color:var(--w);color:#fff;box-shadow:0 3px 12px rgba(123,30,46,.24)}
.rcnt{max-width:1360px;margin:.7rem auto 0;padding:0 2rem;font-size:.8rem;color:var(--soft);font-weight:500}
.grid{max-width:1360px;margin:1rem auto;padding:0 2rem 4rem;display:grid;grid-template-columns:repeat(auto-fill,minmax(230px,1fr));gap:1.3rem}

/* TARJETAS DE PRODUCTO */
.card{background:var(--card);border-radius:var(--r);border:1px solid var(--brd);overflow:hidden;box-shadow:0 2px 10px rgba(0,0,0,.06);transition:transform .28s var(--e),box-shadow .28s var(--e);display:flex;flex-direction:column;position:relative}
.card:hover{transform:translateY(-7px);box-shadow:0 18px 48px rgba(0,0,0,.14)}
.card-img{height:190px;position:relative;overflow:hidden;display:flex;align-items:center;justify-content:center}
.card-img img{width:100%;height:100%;object-fit:cover;transition:transform .4s ease}
.card:hover .card-img img{transform:scale(1.05)}
.card-overlay{position:absolute;inset:0;background:rgba(0,0,0,.55);display:flex;align-items:center;justify-content:center;opacity:0;transition:opacity .25s var(--e);z-index:2}
.card:hover .card-overlay{opacity:1}
.overlay-btn{background:#fff;color:var(--w);border:none;padding:.55rem 1.3rem;border-radius:50px;font-weight:800;font-size:.82rem;transform:translateY(8px);transition:transform .25s var(--e)}
.card:hover .overlay-btn{transform:translateY(0)}
.card-badges{position:absolute;top:10px;left:10px;display:flex;flex-direction:column;gap:.25rem;z-index:3}
.badge{display:inline-block;padding:.2rem .6rem;border-radius:50px;font-size:.65rem;font-weight:700;text-transform:uppercase;backdrop-filter:blur(6px)}
.bc{background:rgba(254,243,199,.95);color:#92400e}
.bt{background:rgba(209,250,229,.95);color:#065f46}
.be{background:rgba(237,233,254,.95);color:#4c1d95}
.bn{background:rgba(212,168,67,.92);color:#4F1320}
.card-body{padding:1.1rem 1.2rem;flex:1;display:flex;flex-direction:column}
.card-name{font-size:.97rem;font-weight:700;color:var(--txt);line-height:1.35;display:-webkit-box;-webkit-line-clamp:2;-webkit-box-orient:vertical;overflow:hidden;min-height:2.6rem}
.card-price{font-family:'Playfair Display',serif;font-size:1.3rem;font-weight:700;color:var(--w);margin-top:auto;padding-top:.7rem}
.card-price small{font-family:'Inter',sans-serif;font-size:.7rem;font-weight:600;color:var(--soft);vertical-align:super}
.card-foot{padding:.75rem 1.2rem 1rem;border-top:1px solid #f2f0ed}
.btn-add{width:100%;padding:.62rem;border:none;border-radius:var(--rs);background:linear-gradient(135deg,var(--w),var(--wd));color:#fff;font-weight:700;font-size:.84rem;box-shadow:0 3px 10px rgba(123,30,46,.22);transition:all .22s var(--e);display:flex;align-items:center;justify-content:center;gap:.4rem}
.btn-add svg{width:15px;height:15px;stroke:#fff;stroke-width:2.2;fill:none}
.btn-add:hover{background:linear-gradient(135deg,var(--wl),var(--w));transform:scale(1.02)}
.btn-add.ok{background:linear-gradient(135deg,#059669,#047857)}
.nores{grid-column:1/-1;text-align:center;padding:5rem 2rem;color:var(--soft)}
.nores h3{font-size:1.1rem;font-weight:700;color:var(--txt);margin-top:1rem}

/* MAGAZINE SECTION */
.mag{background:linear-gradient(135deg,#100509 0%,var(--wd) 100%);padding:4rem 2rem}
.mag-in{max-width:900px;margin:0 auto;text-align:center}
.mag-tag{display:inline-block;background:rgba(212,168,67,.2);border:1px solid rgba(212,168,67,.3);color:var(--gl);padding:.3rem .9rem;border-radius:50px;font-size:.72rem;font-weight:700;text-transform:uppercase;margin-bottom:1.3rem}
.mag h2{font-family:'Playfair Display',serif;font-size:clamp(1.6rem,3.5vw,2.4rem);color:#fff;margin-bottom:1.2rem}
.mag p{color:rgba(255,255,255,.72);line-height:1.85;font-size:1rem;max-width:680px;margin:0 auto 2.5rem}
.mag-cards{display:grid;grid-template-columns:repeat(auto-fit,minmax(220px,1fr));gap:1.2rem}
.mc{background:rgba(255,255,255,.07);backdrop-filter:blur(12px);border:1px solid rgba(255,255,255,.12);border-radius:var(--r);padding:1.6rem 1.3rem;text-align:center;transition:all .25s var(--e)}
.mc:hover{background:rgba(255,255,255,.12);transform:translateY(-4px)}
.mc-ico{width:52px;height:52px;background:rgba(212,168,67,.18);border-radius:14px;display:flex;align-items:center;justify-content:center;margin:0 auto 1rem}
.mc-ico svg{width:26px;height:26px;stroke:var(--gl);stroke-width:1.7;fill:none}
.mc h3{font-size:.95rem;font-weight:700;color:#fff;margin-bottom:.5rem}
.mc p{font-size:.82rem;color:rgba(255,255,255,.62);line-height:1.65}

/* FOOTER */
footer{background:#0e060a;color:rgba(255,255,255,.65);padding:3rem 2rem 1.5rem}
.foot-in{max-width:1360px;margin:0 auto;display:grid;grid-template-columns:2fr 1fr 1fr;gap:3rem}
.f-brand{font-family:'Playfair Display',serif;font-size:1.4rem;color:#fff;font-weight:800;margin-bottom:.6rem}
.f-desc{font-size:.85rem;line-height:1.75;opacity:.72;margin-bottom:1.2rem}
.f-social{display:flex;gap:.7rem}
.fs{width:36px;height:36px;border-radius:50%;border:1px solid rgba(255,255,255,.18);display:flex;align-items:center;justify-content:center;transition:all .2s var(--e)}
.fs:hover{background:var(--w);border-color:var(--w)}
.fs svg{width:16px;height:16px;stroke:rgba(255,255,255,.75);stroke-width:1.8;fill:none}
.f-col h4{font-size:.8rem;font-weight:700;color:#fff;margin-bottom:.9rem;text-transform:uppercase;letter-spacing:1px}
.f-col ul{list-style:none;display:flex;flex-direction:column;gap:.55rem}
.f-col ul a{font-size:.82rem;opacity:.65;transition:opacity .2s}
.f-col ul a:hover{opacity:1}
.foot-bot{max-width:1360px;margin:2rem auto 0;padding-top:1.2rem;border-top:1px solid rgba(255,255,255,.07);display:flex;justify-content:space-between;flex-wrap:wrap;gap:.5rem;font-size:.75rem;opacity:.4}

/* CART DRAWER */
.ovl{display:none;position:fixed;inset:0;background:rgba(0,0,0,.55);backdrop-filter:blur(5px);z-index:500;justify-content:flex-end}
.ovl.on{display:flex;animation:fadeO .22s var(--e)}
@keyframes fadeO{from{opacity:0}to{opacity:1}}
.drawer{width:440px;max-width:100vw;background:#fff;display:flex;flex-direction:column;animation:slideD .3s var(--e);box-shadow:-8px 0 40px rgba(0,0,0,.15)}
@keyframes slideD{from{transform:translateX(100%)}to{transform:translateX(0)}}
.d-head{padding:1.3rem 1.5rem;border-bottom:1px solid var(--brd);display:flex;justify-content:space-between;align-items:center}
.d-title{display:flex;align-items:center;gap:.6rem}
.d-title h2{font-size:1.1rem;font-weight:800}
.d-cnt{background:var(--w);color:#fff;border-radius:50px;padding:.1rem .5rem;font-size:.72rem;font-weight:700}
.d-x{background:#f5f2ef;border:none;width:32px;height:32px;border-radius:50%;display:flex;align-items:center;justify-content:center}
.d-x:hover{background:#ebe7e3}
.d-x svg{width:14px;height:14px;stroke:var(--mid);stroke-width:2.2}
.d-items{flex:1;overflow-y:auto;padding:1rem 1.5rem}
.ci{display:flex;align-items:center;gap:.9rem;padding:.85rem 0;border-bottom:1px solid #f5f2ef}
.ci-thumb{width:46px;height:46px;border-radius:10px;background-size:cover;background-position:center;flex-shrink:0}
.ci-info{flex:1}
.ci-name{font-weight:700;font-size:.86rem;white-space:nowrap;overflow:hidden;text-overflow:ellipsis}
.ci-unit{font-size:.74rem;color:var(--soft)}
.ci-price{font-weight:800;font-size:.92rem;color:var(--w)}
.qty{display:flex;align-items:center;gap:.25rem;background:#f5f2ef;border-radius:50px;padding:.15rem .25rem}
.qb{background:none;border:none;width:24px;height:24px;border-radius:50%;display:flex;align-items:center;justify-content:center;font-size:1rem;font-weight:700;cursor:pointer}
.qb:hover{background:#e5e1db}
.qb.m:hover{background:#fee2e2;color:#ef4444}
.qn{font-weight:700;font-size:.85rem;min-width:20px;text-align:center}
.d-empty{display:flex;flex-direction:column;align-items:center;justify-content:center;height:100%;padding:3rem;text-align:center;color:var(--soft)}
.d-foot{padding:1.2rem 1.5rem;border-top:1px solid var(--brd);background:#faf8f6}
.sums{display:flex;flex-direction:column;gap:.35rem;margin-bottom:1rem}
.sum-r{display:flex;justify-content:space-between;font-size:.86rem}
.sum-r.tot span:first-child{font-weight:700;font-size:.95rem;color:var(--txt)}
.sum-r.tot span:last-child{font-family:'Playfair Display',serif;font-size:1.35rem;font-weight:700;color:var(--w)}
.d-acts{display:flex;flex-direction:column;gap:.55rem}
.btn-wa{display:flex;align-items:center;justify-content:center;gap:.55rem;background:linear-gradient(135deg,#25D366,#128C7E);color:#fff;border:none;padding:.95rem;border-radius:var(--rs);font-weight:700;font-size:.95rem;transition:all .22s var(--e)}
.btn-wa:hover{transform:translateY(-2px)}
.btn-wa svg{width:20px;height:20px;fill:#fff}
.btn-clr{background:none;border:1.5px solid var(--brd);color:var(--soft);padding:.65rem;border-radius:var(--rs);font-size:.82rem;font-weight:600}
.btn-clr:hover{border-color:#fca5a5;color:#ef4444;background:#fff5f5}
.toasts{position:fixed;bottom:2rem;right:2rem;z-index:999;display:flex;flex-direction:column;gap:.55rem}
.toast{background:#fff;border-radius:12px;padding:.8rem 1.1rem;box-shadow:0 8px 28px rgba(0,0,0,.12);display:flex;align-items:center;gap:.6rem;font-weight:600;font-size:.86rem;border-left:4px solid #10b981;animation:tIn .28s var(--e)}
.toast svg{width:18px;height:18px;stroke:#10b981;stroke-width:2.2}
@keyframes tIn{from{opacity:0;transform:translateX(70px)}to{opacity:1;transform:translateX(0)}}
.toast.out{animation:tOut .25s var(--e) forwards}
@keyframes tOut{to{opacity:0;transform:translateX(70px)}}

/* PRODUCT MODAL */
.pm-ovl{display:none;position:fixed;inset:0;background:rgba(0,0,0,.65);backdrop-filter:blur(8px);z-index:600;align-items:center;justify-content:center;padding:1rem}
.pm-ovl.on{display:flex}
.pm-box{background:#fff;border-radius:20px;width:100%;max-width:680px;max-height:90vh;overflow-y:auto;animation:pmIn .32s var(--e)}
@keyframes pmIn{from{opacity:0;transform:scale(.93) translateY(20px)}to{opacity:1;transform:none}}
.pm-img{height:260px;position:relative;overflow:hidden;border-radius:20px 20px 0 0}
.pm-img img{width:100%;height:100%;object-fit:cover}
.pm-close{position:absolute;top:14px;right:14px;background:rgba(0,0,0,.35);backdrop-filter:blur(6px);border:none;width:34px;height:34px;border-radius:50%;display:flex;align-items:center;justify-content:center;cursor:pointer}
.pm-close svg{width:14px;height:14px;stroke:#fff;stroke-width:2.5}
.pm-body{padding:1.8rem}
.pm-cat{display:inline-flex;align-items:center;gap:.4rem;padding:.28rem .8rem;border-radius:50px;font-size:.72rem;font-weight:700;text-transform:uppercase;margin-bottom:.9rem}
.pm-name{font-family:'Playfair Display',serif;font-size:1.6rem;font-weight:800;color:var(--txt);margin-bottom:.4rem}
.pm-price{font-family:'Playfair Display',serif;font-size:2rem;font-weight:800;color:var(--w);margin-bottom:1.2rem}
.pm-price small{font-family:'Inter',sans-serif;font-size:.8rem;font-weight:600;vertical-align:super}
.pm-tags{display:flex;gap:.6rem;flex-wrap:wrap;margin-bottom:1.2rem}
.pm-tag{display:flex;align-items:center;gap:.35rem;background:#f6f4f1;border-radius:50px;padding:.35rem .9rem;font-size:.78rem;font-weight:600;color:var(--mid)}
.pm-tag svg{width:14px;height:14px;stroke:var(--w);stroke-width:2}
.pm-desc-title{font-size:.78rem;font-weight:700;text-transform:uppercase;letter-spacing:1px;color:var(--soft);margin-bottom:.55rem}
.pm-desc{font-size:.92rem;line-height:1.8;color:var(--mid);margin-bottom:1.5rem}
.pm-add{width:100%;padding:.9rem;border:none;border-radius:var(--rs);background:linear-gradient(135deg,var(--w),var(--wd));color:#fff;font-weight:700;font-size:1rem;transition:all .22s var(--e);display:flex;align-items:center;justify-content:center;gap:.5rem}
.pm-add:hover{transform:scale(1.02)}
.pm-add.ok{background:linear-gradient(135deg,#059669,#047857)}
.coupon-row{display:flex;gap:.5rem;margin-bottom:.9rem}
.coupon-input{flex:1;padding:.6rem .9rem;border:1.5px solid var(--brd);border-radius:var(--rs);font-size:.84rem;background:#faf8f6}
.coupon-input:focus{outline:none;border-color:var(--w)}
.coupon-apply{background:var(--w);color:#fff;border:none;padding:.6rem 1rem;border-radius:var(--rs);font-weight:700;font-size:.8rem}
.discount-row{background:#f0fdf4;border:1px solid #bbf7d0;border-radius:var(--rs);padding:.6rem .9rem;display:flex;justify-content:space-between;align-items:center;font-size:.84rem;margin-bottom:.6rem}
.discount-row button{background:none;border:none;color:#dc2626;cursor:pointer;padding:0 .2rem}
@media(max-width:900px){.slider{height:70vh}.foot-in{grid-template-columns:1fr 1fr}}
@media(max-width:600px){.hdr{padding:.75rem 1rem;gap:.6rem}.srch{order:3;flex-basis:100%;max-width:100%}.logo-sub,.nav-links-wrap{display:none}.grid{grid-template-columns:repeat(2,1fr);gap:1rem;padding:0 1rem 3rem}.trust-in{gap:1rem}.mag-cards{grid-template-columns:1fr 1fr}.foot-in{grid-template-columns:1fr}.sl-arrow{display:none}}
@media(max-width:380px){.grid{grid-template-columns:1fr}}
</style>
</head>
<body>

<div class="topbar">🚚 <strong>Entregas en La Paz y envíos a todo Bolivia</strong> — Consultá por WhatsApp · Todos los precios en Bs</div>

<header id="hdr">
  <div class="hdr">
    <div class="logo">
      <div class="logo-ico"><svg viewBox="0 0 24 24"><path d="M12 2L2 7l10 5 10-5-10-5z"/><path d="M2 17l10 5 10-5M2 12l10 5 10-5"/></svg></div>
      <div class="logo-t"><span class="logo-name">Aynigames</span><span class="logo-sub">Catálogo Profesional</span></div>
    </div>
    <div class="srch"><svg viewBox="0 0 24 24"><circle cx="11" cy="11" r="8"/><path d="m21 21-4.35-4.35"/></svg><input type="text" id="si" placeholder="Buscar juegos..." autocomplete="off"></div>
    <nav class="links nav-links-wrap"><a class="nl" href="#">Inicio</a><a class="nl" href="#catalogo">Catálogo</a><a class="nl" href="#" onclick="sendWAConsulta()">Contacto</a></nav>
    <button class="cart-b" id="cb" onclick="openCart()"><svg viewBox="0 0 24 24"><path d="M6 2 3 6v14a2 2 0 0 0 2 2h14a2 2 0 0 0 2-2V6l-3-4z"/><line x1="3" y1="6" x2="21" y2="6"/><path d="M16 10a4 4 0 0 1-8 0"/></svg>Carrito <span class="cbadge" id="cc">0</span></button>
  </div>
</header>

<div class="slider" id="slider">
  <div class="slides" id="slides">
    <div class="slide active"><div class="slide-bg" style="background-image:url('https://images.unsplash.com/photo-1610890716171-6b1bb98ffd09?w=1600&h=900&fit=crop')"></div><div class="slide-overlay"></div><div class="slide-content"><div class="slide-tag">⭐ Estrategia</div><h2>Domina el tablero,<br><em>conquista Bolivia</em></h2><p>Desafíos de estrategia para mentes brillantes.</p><div class="slide-btns"><button class="btn-gold" onclick="filt('estrategia',document.getElementById('ch-e'));document.getElementById('catalogo').scrollIntoView({behavior:'smooth'})">Ver Estrategia →</button><button class="btn-ghost" onclick="sendWAConsulta()">💬 Asesorarme</button></div></div></div>
    <div class="slide"><div class="slide-bg" style="background-image:url('https://images.unsplash.com/photo-1611996575748-6f0be1e7b5c9?w=1600&h=900&fit=crop')"></div><div class="slide-overlay"></div><div class="slide-content"><div class="slide-tag">🃏 Cartas</div><h2>La diversión cabe<br>en <em>tus manos</em></h2><p>Exploding Kittens, Dixit, Secret Hitler y más.</p><div class="slide-btns"><button class="btn-gold" onclick="filt('cartas',document.getElementById('ch-c'));document.getElementById('catalogo').scrollIntoView({behavior:'smooth'})">Ver Cartas →</button><button class="btn-ghost" onclick="sendWAConsulta()">💬 Consultar</button></div></div></div>
    <div class="slide"><div class="slide-bg" style="background-image:url('https://images.unsplash.com/photo-1534422298391-e4f8c172dddb?w=1600&h=900&fit=crop')"></div><div class="slide-overlay"></div><div class="slide-content"><div class="slide-tag">🗺️ Tablero</div><h2>Grandes aventuras<br><em>sobre la mesa</em></h2><p>Azul, Carcassonne, Ticket to Ride y más.</p><div class="slide-btns"><button class="btn-gold" onclick="filt('tablero',document.getElementById('ch-b'));document.getElementById('catalogo').scrollIntoView({behavior:'smooth'})">Ver Tablero →</button><button class="btn-ghost" onclick="sendWAConsulta()">💬 Consultar</button></div></div></div>
    <div class="slide"><div class="slide-bg" style="background-image:url('https://images.unsplash.com/photo-1586899028174-e709b1e3f9f8?w=1600&h=900&fit=crop')"></div><div class="slide-overlay"></div><div class="slide-content"><div class="slide-tag">🎲 Aynigames Bolivia</div><h2>La mejor tienda<br>de juegos de mesa en <em>Bolivia</em></h2><p>Más de 70 juegos disponibles. Asesoramiento personalizado.</p><div class="slide-btns"><button class="btn-gold" onclick="document.getElementById('catalogo').scrollIntoView({behavior:'smooth'})">Ver Catálogo →</button><button class="btn-ghost" onclick="sendWAConsulta()">💬 WhatsApp</button></div></div></div>
  </div>
  <button class="sl-arrow sl-prev" onclick="slMove(-1)"><svg viewBox="0 0 24 24"><polyline points="15 18 9 12 15 6"/></svg></button>
  <button class="sl-arrow sl-next" onclick="slMove(1)"><svg viewBox="0 0 24 24"><polyline points="9 18 15 12 9 6"/></svg></button>
  <div class="sl-dots" id="slDots"></div>
</div>

<div class="trust">
  <div class="trust-in">
    <div class="ti"><div class="ti-ico"><svg viewBox="0 0 24 24"><rect x="1" y="3" width="15" height="13"/><polygon points="16 8 20 8 23 11 23 16 16 16 16 8"/><circle cx="5.5" cy="18.5" r="2.5"/><circle cx="18.5" cy="18.5" r="2.5"/></svg></div><div><strong>Envíos a todo el pais</strong><span>A consultar por zona</span></div></div>
    <div class="ti"><div class="ti-ico"><svg viewBox="0 0 24 24"><rect x="1" y="4" width="22" height="16" rx="2" ry="2"/><line x1="1" y1="10" x2="23" y2="10"/></svg></div><div><strong>Formas de pago</strong><span>Efectivo · Transferencia</span></div></div>
    <div class="ti"><div class="ti-ico"><svg viewBox="0 0 24 24"><path d="M21 15a2 2 0 0 1-2 2H7l-4 4V5a2 2 0 0 1 2-2h14a2 2 0 0 1 2 2z"/></svg></div><div><strong>Asesoramiento</strong><span>Te ayudamos a elegir</span></div></div>
    <div class="ti"><div class="ti-ico"><svg viewBox="0 0 24 24"><path d="M12 22s8-4 8-10V5l-8-3-8 3v7c0 6 8 10 8 10z"/></svg></div><div><strong>Ediciones de importación</strong><span>Calidad Internacional</span></div></div>
  </div>
</div>

<div class="sec-hdr" id="catalogo">
  <div><h2 class="sec-h2">Nuestro <span>Catálogo</span></h2><p class="sec-sub">Filtrá por categoría o buscá tu juego favorito</p></div>
  <div class="filters" style="padding:0">
    <button class="chip on" id="ch-t" onclick="filt('todos',this)">🎮 Todos</button>
    <button class="chip" id="ch-c" onclick="filt('cartas',this)">🃏 Cartas</button>
    <button class="chip" id="ch-b" onclick="filt('tablero',this)">🗺️ Tablero</button>
    <button class="chip" id="ch-e" onclick="filt('estrategia',this)">🧠 Estrategia</button>
  </div>
</div>
<p class="rcnt" id="rc"></p>
<div class="grid" id="grid"></div>

<section class="mag">
  <div class="mag-in">
    <div class="mag-tag">📖 Experiencia de Juego</div>
    <h2>¿Por qué elegir un juego de mesa?</h2>
    <p>Los juegos de mesa desarrollan el pensamiento estratégico, fortalecen lazos familiares y crean recuerdos únicos.</p>
    <div class="mag-cards">
      <div class="mc"><div class="mc-ico"><svg viewBox="0 0 24 24"><path d="M17 21v-2a4 4 0 0 0-4-4H5a4 4 0 0 0-4 4v2"/><circle cx="9" cy="7" r="4"/><path d="M23 21v-2a4 4 0 0 0-3-3.87"/><path d="M16 3.13a4 4 0 0 1 0 7.75"/></svg></div><h3>Para toda la familia</h3><p>Juegos para todas las edades y niveles.</p></div>
      <div class="mc"><div class="mc-ico"><svg viewBox="0 0 24 24"><polygon points="12 2 15.09 8.26 22 9.27 17 14.14 18.18 21.02 12 17.77 5.82 21.02 7 14.14 2 9.27 8.91 8.26 12 2"/></svg></div><h3>Títulos premiados</h3><p>Selección de los mejores juegos del mundo.</p></div>
      <div class="mc"><div class="mc-ico"><svg viewBox="0 0 24 24"><path d="M21 15a2 2 0 0 1-2 2H7l-4 4V5a2 2 0 0 1 2-2h14a2 2 0 0 1 2 2z"/></svg></div><h3>Asesoramiento experto</h3><p>Te ayudamos a encontrar el juego ideal.</p></div>
    </div>
  </div>
</section>

<footer>
  <div class="foot-in">
    <div><div class="f-brand">🎲 Aynigames</div><p class="f-desc">Especialistas en juegos de mesa en Bolivia. Los mejores títulos para disfrutar en familia.</p><div class="f-social"><a class="fs" href="#"><svg viewBox="0 0 24 24"><rect x="2" y="2" width="20" height="20" rx="5"/><path d="M16 11.37A4 4 0 1 1 12.63 8 4 4 0 0 1 16 11.37z"/><line x1="17.5" y1="6.5" x2="17.51" y2="6.5"/></svg></a><a class="fs" href="#"><svg viewBox="0 0 24 24"><path d="M18 2h-3a5 5 0 0 0-5 5v3H7v4h3v8h4v-8h3l1-4h-4V7a1 1 0 0 1 1-1h3z"/></svg></a><a class="fs" href="#" onclick="sendWAConsulta()"><svg viewBox="0 0 24 24"><path d="M21 15a2 2 0 0 1-2 2H7l-4 4V5a2 2 0 0 1 2-2h14a2 2 0 0 1 2 2z"/></svg></a></div></div>
    <div class="f-col"><h4>Catálogo</h4><ul><li><a href="#" onclick="filt('todos',document.getElementById('ch-t'))">Todos</a></li><li><a href="#" onclick="filt('cartas',document.getElementById('ch-c'))">Cartas</a></li><li><a href="#" onclick="filt('tablero',document.getElementById('ch-b'))">Tablero</a></li><li><a href="#" onclick="filt('estrategia',document.getElementById('ch-e'))">Estrategia</a></li></ul></div>
    <div class="f-col"><h4>Info</h4><ul><li><a href="#">Cómo elegir un juego</a></li><li><a href="#">Formas de pago</a></li><li><a href="#">Política de envíos</a></li><li><a href="#" onclick="sendWAConsulta()">Contacto</a></li></ul></div>
  </div>
  <div class="foot-bot"><span>© 2025 Aynigames — Todos los derechos reservados</span><span>asión por los juegos de mesa desde Bolivia con ❤️</span></div>
</footer>

<!-- DRAWER CARRITO, MODAL PRODUCTO, TOASTS -->
<div class="ovl" id="ovl" onclick="closeOnBg(event)"><div class="drawer"><div class="d-head"><div class="d-title"><svg style="width:18px;height:18px;stroke:var(--w);stroke-width:2;fill:none" viewBox="0 0 24 24"><path d="M6 2 3 6v14a2 2 0 0 0 2 2h14a2 2 0 0 0 2-2V6l-3-4z"/><line x1="3" y1="6" x2="21" y2="6"/><path d="M16 10a4 4 0 0 1-8 0"/></svg><h2>Tu Carrito</h2><span class="d-cnt" id="dc">0</span></div><button class="d-x" onclick="closeCart()"><svg viewBox="0 0 24 24"><line x1="18" y1="6" x2="6" y2="18"/><line x1="6" y1="6" x2="18" y2="18"/></svg></button></div><div class="d-items" id="di"></div><div class="d-foot" id="df" style="display:none"><div class="coupon-row"><input class="coupon-input" id="cpnInput" placeholder="Código de descuento"><button class="coupon-apply" onclick="applyCoupon()">Aplicar</button></div><div id="cpnResult"></div><div class="sums"><div class="sum-r"><span>Subtotal</span><span id="st">Bs 0</span></div><div class="sum-r" id="discRow" style="display:none"><span style="color:#16a34a;font-weight:700">Descuento</span><span id="discAmt" style="color:#16a34a;font-weight:700"></span></div><div class="sum-r tot"><span>Total</span><span id="gt">Bs 0</span></div></div><div class="d-acts"><button class="btn-wa" onclick="sendWA()"><svg viewBox="0 0 24 24" style="width:20px;height:20px;fill:#fff"><path d="M17.472 14.382c-.297-.149-1.758-.867-2.03-.967-.273-.099-.471-.148-.67.15-.197.297-.767.966-.94 1.164-.173.199-.347.223-.644.075-.297-.15-1.255-.463-2.39-1.475-.883-.788-1.48-1.761-1.653-2.059-.173-.297-.018-.458.13-.606.134-.133.298-.347.446-.52.149-.174.198-.298.298-.497.099-.198.05-.371-.025-.52-.075-.149-.669-1.612-.916-2.207-.242-.579-.487-.5-.669-.51-.173-.008-.371-.01-.57-.01-.198 0-.52.074-.792.372-.272.297-1.04 1.016-1.04 2.479 0 1.462 1.065 2.875 1.213 3.074.149.198 2.096 3.2 5.077 4.487.709.306 1.262.489 1.694.625.712.227 1.36.195 1.871.118.571-.085 1.758-.719 2.006-1.413.248-.694.248-1.289.173-1.413-.074-.124-.272-.198-.57-.347m-5.421 7.403h-.004a9.87 9.87 0 01-5.031-1.378l-.361-.214-3.741.982.998-3.648-.235-.374a9.86 9.86 0 01-1.51-5.26c.001-5.45 4.436-9.884 9.888-9.884 2.64 0 5.122 1.03 6.988 2.898a9.825 9.825 0 012.893 6.994c-.003 5.45-4.437 9.884-9.885 9.884m8.413-18.297A11.815 11.815 0 0012.05 0C5.495 0 .16 5.335.157 11.892c0 2.096.547 4.142 1.588 5.945L.057 24l6.305-1.654a11.882 11.882 0 005.683 1.448h.005c6.554 0 11.89-5.335 11.893-11.893a11.821 11.821 0 00-3.48-8.413z"/></svg>Pedir por WhatsApp</button><button class="btn-clr" onclick="clearCart()">🗑️ Vaciar carrito</button></div></div></div></div>
<div class="toasts" id="tw"></div>
<div class="pm-ovl" id="pmOvl" onclick="closePM(event)"><div class="pm-box" id="pmBox"></div></div>

<script>
// ==================== LISTA COMPLETA DE JUEGOS (con imágenes de postimg.cc y Spot It incluidos) ====================
const P = [
  {n:"7 Wonders",p:335,c:"estrategia",e:"🧠",new:false,img:"https://i.postimg.cc/J4Snrn0w/7-wonders.png"},
  {n:"7 Wonders Duel",p:330,c:"estrategia",e:"🧠",new:false,img:"https://i.postimg.cc/KYPzhPQV/image.png"},
  {n:"7 Wonders 2da edicion limitada",p:690,c:"estrategia",e:"🧠",new:true,img:"https://i.postimg.cc/BQQ6FPpM/image.png"},
  {n:"Avalon",p:230,c:"cartas",e:"🃏",new:false,img:"https://i.postimg.cc/7PdpSfgT/image.png"},
  {n:"Azul",p:380,c:"tablero",e:"🗺️",new:false,img:"https://i.postimg.cc/Rhghbw4q/image.png"},
  {n:"Azul Summer Pavillion",p:410,c:"tablero",e:"🗺️",new:true,img:"https://i.postimg.cc/MKrSTqDr/image.png"},
  {n:"Bears vs Babies",p:240,c:"cartas",e:"🃏",new:false,img:"https://i.postimg.cc/VsDRnTn9/image.png"},
  {n:"Bears vs Babies EXP",p:95,c:"cartas",e:"🃏",new:false,img:"https://i.postimg.cc/VkL2XT7j/image.png"},
  {n:"Beat That",p:340,c:"tablero",e:"🗺️",new:false,img:"https://i.postimg.cc/0jtW25pd/image.png"},
  {n:"Barking Kittens",p:190,c:"cartas",e:"🃏",new:false,img:"https://i.postimg.cc/Yqzv7VYQ/image.png"},
  {n:"Carcassone",p:360,c:"tablero",e:"🗺️",new:false,img:"https://i.postimg.cc/3J5GYm6H/image.png"},
  {n:"Catan",p:315,c:"estrategia",e:"🧠",new:false,img:"https://i.postimg.cc/yNvhNxRn/image.png"},
  {n:"Catan Extension",p:210,c:"estrategia",e:"🧠",new:false,img:"https://i.postimg.cc/QdP9Y7cn/image.png"},
  {n:"Catan Navegantes",p:380,c:"estrategia",e:"🧠",new:false,img:"https://i.postimg.cc/sX8GqhFj/image.png"},
  {n:"Catan Navegantes Ext",p:290,c:"estrategia",e:"🧠",new:false,img:"https://i.postimg.cc/Xqmmz3kV/image.png"},
  {n:"Cities of Splendor",p:360,c:"estrategia",e:"🧠",new:true,img:"https://i.postimg.cc/K8Zwp9n5/image.png"},
  {n:"Clank",p:500,c:"tablero",e:"🗺️",new:false,img:"https://i.postimg.cc/pXynQvSn/image.png"},
  {n:"Código Secreto",p:280,c:"cartas",e:"🃏",new:false,img:"https://i.postimg.cc/L4PsmsGw/image.png"},
  {n:"Coup",p:160,c:"cartas",e:"🃏",new:false,img:"https://i.postimg.cc/zv0BkHNQ/image.png"},
  {n:"Dixit",p:340,c:"cartas",e:"🃏",new:false,img:"https://i.postimg.cc/xCFH0ZJr/image.png"},
  {n:"Dixit Quest EXP",p:210,c:"cartas",e:"🃏",new:false,img:"https://i.postimg.cc/bwXMTyYP/image.png"},
  {n:"Dixit Stella",p:360,c:"cartas",e:"🃏",new:true,img:"https://i.postimg.cc/XNdDvMcK/image.png"},
  {n:"Exploding Kittens Party",p:190,c:"cartas",e:"🃏",new:false,img:"https://i.postimg.cc/HxqY9GV3/image.png"},
  {n:"Exploding Kittens",p:175,c:"cartas",e:"🃏",new:false,img:"https://i.postimg.cc/bY9WTcDw/image.png"},
  {n:"Exploding Minions",p:150,c:"cartas",e:"🃏",new:false,img:"https://i.postimg.cc/Pr8ZHhWm/image.png"},
  {n:"Exploding Kittens NSFW",p:160,c:"cartas",e:"🃏",new:false,img:"https://i.postimg.cc/7LPddKpc/image.png"},
  {n:"Fantasma Blitz",p:150,c:"cartas",e:"🃏",new:false,img:"https://i.postimg.cc/ZnLqb753/image.png"},
  {n:"Happy Little Dinosaurs",p:320,c:"cartas",e:"🃏",new:false,img:"https://i.postimg.cc/9FRL46h0/image.png"},
  {n:"Happy Little Dinosaurs Expansion",p:280,c:"cartas",e:"🃏",new:false,img:"https://i.postimg.cc/R0sPJ4N7/image.png"},
  {n:"Hombre Lobo",p:160,c:"cartas",e:"🃏",new:false,img:"https://i.postimg.cc/05w1F7Pq/image.png"},
  {n:"Imploding Streaking",p:190,c:"cartas",e:"🃏",new:false,img:"https://i.postimg.cc/RVCy9YHv/image.png"},
  {n:"Jaipur",p:230,c:"cartas",e:"🃏",new:false,img:"https://i.postimg.cc/Dfx5QwSz/image.png"},
  {n:"Monopolio Games of Thrones",p:360,c:"tablero",e:"🗺️",new:false,img:"https://i.postimg.cc/7Lp1t5gm/image.png"},
  {n:"Pandemic",p:320,c:"estrategia",e:"🧠",new:false,img:"https://i.postimg.cc/8CPP84bV/image.png"},
  {n:"Patchwork",p:240,c:"tablero",e:"🗺️",new:false,img:"https://i.postimg.cc/mrtfN5wS/image.png"},
  {n:"Phase 10",p:50,c:"cartas",e:"🃏",new:false,img:"https://i.postimg.cc/SQ5rJtXw/image.png"},
  {n:"Play Nine",p:230,c:"cartas",e:"🃏",new:false,img:"https://i.postimg.cc/VNpqdJv4/image.png"},
  {n:"Race to the Treasure",p:210,c:"tablero",e:"🗺️",new:false,img:"https://i.postimg.cc/1RJzHL0L/image.png"},
  {n:"Root",p:575,c:"estrategia",e:"🧠",new:false,img:"https://i.postimg.cc/cJpFP9Rx/image.png"},
  {n:"Root Ribereños",p:430,c:"estrategia",e:"🧠",new:true,img:"https://i.postimg.cc/9F2Qccmm/image.png"},
  {n:"Saboteur",p:170,c:"cartas",e:"🃏",new:false,img:"https://i.postimg.cc/Hk7Z31Mb/image.png"},
  {n:"Secret Hitler",p:350,c:"cartas",e:"🃏",new:false,img:"https://i.postimg.cc/fLk0jDtQ/image.png"},
  {n:"Sequence",p:260,c:"tablero",e:"🗺️",new:false,img:"https://i.postimg.cc/L8tgphTT/image.png"},
  {n:"Sequence for Kids",p:230,c:"tablero",e:"🗺️",new:false,img:"https://i.postimg.cc/KYXXn8Sw/image.png"},
  {n:"Splendor",p:350,c:"estrategia",e:"🧠",new:false,img:"https://i.postimg.cc/tgzrYqqQ/image.png"},
  {n:"Splendor Marvel",p:390,c:"estrategia",e:"🧠",new:false,img:"https://i.postimg.cc/pLJ7nYCq/image.png"},
  {n:"Sushi GO Party",p:320,c:"cartas",e:"🃏",new:false,img:"https://i.postimg.cc/76kfQ47p/image.png"},
  {n:"Terraforming Mars",p:690,c:"estrategia",e:"🧠",new:false,img:"https://i.postimg.cc/Gm6WRhXV/image.png"},
  {n:"The Mind",p:150,c:"cartas",e:"🃏",new:false,img:"https://i.postimg.cc/zBz0Zs1D/image.png"},
  {n:"Ticket to Ride Europa",p:360,c:"tablero",e:"🗺️",new:false,img:"https://i.postimg.cc/FHF6Qkby/image.png"},
  {n:"Ticket to Ride for Journey",p:320,c:"tablero",e:"🗺️",new:false,img:"https://i.postimg.cc/q7RW26z7/image.png"},
  {n:"Ticket to Ride USA",p:360,c:"tablero",e:"🗺️",new:false,img:"https://i.postimg.cc/m2kMfbzm/image.png"},
  {n:"Throw Throw Burrito",p:380,c:"cartas",e:"🃏",new:true,img:"https://i.postimg.cc/k50RW8fy/image.png"},
  {n:"Wingspan",p:690,c:"estrategia",e:"🧠",new:false,img:"https://i.postimg.cc/JhpMLWBs/image.png"},
  {n:"Zombie Kittens",p:170,c:"cartas",e:"🃏",new:false,img:"https://i.postimg.cc/cL4d5HrV/image.png"},
  // ==================== SPOT IT (15 juegos) ====================
  {n:"Spot It Marvel",p:99,c:"cartas",e:"🃏",new:false,img:"https://images.unsplash.com/photo-1587654780291-39c9404d746b?w=400&h=300&fit=crop"},
  {n:"Spot It Harry Potter",p:99,c:"cartas",e:"🃏",new:false,img:"https://images.unsplash.com/photo-1587654780291-39c9404d746b?w=400&h=300&fit=crop"},
  {n:"Spot It Disney 100 Años",p:99,c:"cartas",e:"🃏",new:true,img:"https://images.unsplash.com/photo-1587654780291-39c9404d746b?w=400&h=300&fit=crop"},
  {n:"Spot It 123",p:99,c:"cartas",e:"🃏",new:false,img:"https://images.unsplash.com/photo-1587654780291-39c9404d746b?w=400&h=300&fit=crop"},
  {n:"Spot It Princesas",p:99,c:"cartas",e:"🃏",new:false,img:"https://images.unsplash.com/photo-1587654780291-39c9404d746b?w=400&h=300&fit=crop"},
  {n:"Spot It Cars",p:99,c:"cartas",e:"🃏",new:false,img:"https://images.unsplash.com/photo-1587654780291-39c9404d746b?w=400&h=300&fit=crop"},
  {n:"Spot It Bob Esponja",p:99,c:"cartas",e:"🃏",new:false,img:"https://images.unsplash.com/photo-1587654780291-39c9404d746b?w=400&h=300&fit=crop"},
  {n:"Spot It DC",p:99,c:"cartas",e:"🃏",new:false,img:"https://images.unsplash.com/photo-1587654780291-39c9404d746b?w=400&h=300&fit=crop"},
  {n:"Spot It Holidays",p:99,c:"cartas",e:"🃏",new:false,img:"https://images.unsplash.com/photo-1587654780291-39c9404d746b?w=400&h=300&fit=crop"},
  {n:"Spot It Halloween",p:99,c:"cartas",e:"🃏",new:false,img:"https://images.unsplash.com/photo-1587654780291-39c9404d746b?w=400&h=300&fit=crop"},
  {n:"Spot It Pokémon",p:99,c:"cartas",e:"🃏",new:false,img:"https://images.unsplash.com/photo-1587654780291-39c9404d746b?w=400&h=300&fit=crop"},
  {n:"Spot It Minions",p:99,c:"cartas",e:"🃏",new:false,img:"https://images.unsplash.com/photo-1587654780291-39c9404d746b?w=400&h=300&fit=crop"},
  {n:"Spot It Alfabético",p:99,c:"cartas",e:"🃏",new:false,img:"https://images.unsplash.com/photo-1587654780291-39c9404d746b?w=400&h=300&fit=crop"},
  {n:"Spot It Star Wars",p:99,c:"cartas",e:"🃏",new:false,img:"https://images.unsplash.com/photo-1587654780291-39c9404d746b?w=400&h=300&fit=crop"},
  {n:"Spot It Pixar",p:99,c:"cartas",e:"🃏",new:false,img:"https://images.unsplash.com/photo-1587654780291-39c9404d746b?w=400&h=300&fit=crop"}
];

// ==================== RESTO DEL CÓDIGO JS (localStorage, filtros, carrito, etc.) ====================
let cart = {};
let cf = 'todos';
let st = '';
let activeCoupon = null;
let debounceTimer;

function loadCartFromStorage() { const saved = localStorage.getItem('aynigames_cart'); if (saved) cart = JSON.parse(saved); const savedCat = localStorage.getItem('aynigames_category'); if (savedCat && ['todos','cartas','tablero','estrategia'].includes(savedCat)) { cf = savedCat; document.querySelectorAll('.chip').forEach(ch => ch.classList.remove('on')); if (cf === 'todos') document.getElementById('ch-t').classList.add('on'); if (cf === 'cartas') document.getElementById('ch-c').classList.add('on'); if (cf === 'tablero') document.getElementById('ch-b').classList.add('on'); if (cf === 'estrategia') document.getElementById('ch-e').classList.add('on'); } badge(); render(); }
function saveCartToStorage() { localStorage.setItem('aynigames_cart', JSON.stringify(cart)); }
function saveCategoryToStorage() { localStorage.setItem('aynigames_category', cf); }

const DESC = { cartas:'Juego de cartas rápido y divertido. Ideal para toda la familia. Cada partida es única.', tablero:'Juego de tablero con componentes de alta calidad. Perfecto para noches de juegos.', estrategia:'Juego de estrategia profunda que pondrá a prueba tu mente. Planeá cada movimiento.' };
const INFO = { cartas:['2-6 jugadores','6+ años','15-30 min'], tablero:['2-4 jugadores','8+ años','45-90 min'], estrategia:['2-5 jugadores','10+ años','60-120 min'] };
const BC = { cartas:'bc', tablero:'bt', estrategia:'be' };
const CL = { cartas:'Cartas', tablero:'Tablero', estrategia:'Estrategia' };

function getF() { return P.filter(p => (cf === 'todos' || p.c === cf) && p.n.toLowerCase().includes(st)); }
function render() { const g = document.getElementById('grid'), rc = document.getElementById('rc'), f = getF(); rc.textContent = f.length ? (st || cf !== 'todos' ? `${f.length} ${f.length===1?'juego encontrado':'juegos encontrados'}` : '') : ''; if (!f.length) { g.innerHTML = '<div class="nores"><svg style="width:48px;height:48px;stroke:#d0ccc7;stroke-width:1.5;fill:none" viewBox="0 0 24 24"><circle cx="11" cy="11" r="8"/><path d="m21 21-4.35-4.35"/></svg><h3>No encontramos juegos</h3><p>Probá con otro término o categoría</p></div>'; return; } g.innerHTML = f.map((p, idx) => { const originalIdx = P.findIndex(x => x.n === p.n); const ic = !!cart[p.n]; return `<div class="card"><div class="card-img" onclick="openPM(${originalIdx})"><img src="${p.img}" alt="${p.n}" loading="lazy"><div class="card-overlay"><button class="overlay-btn" onclick="event.stopPropagation();add('${p.n.replace(/'/g,"\\'")}',${p.p},${originalIdx})">${ic?'✓ Agregado':'+ Ver detalle'}</button></div><div class="card-badges"><span class="badge ${BC[p.c]}">${CL[p.c]}</span>${p.new?'<span class="badge bn">Nuevo</span>':''}</div></div><div class="card-body" onclick="openPM(${originalIdx})"><h3 class="card-name">${p.n}</h3><div class="card-price"><small>Bs </small>${p.p}</div></div><div class="card-foot"><button class="btn-add${ic?' ok':''}" onclick="add('${p.n.replace(/'/g,"\\'")}',${p.p},${originalIdx})"><svg viewBox="0 0 24 24">${ic?'<polyline points="20 6 9 17 4 12"/>':'<line x1="12" y1="5" x2="12" y2="19"/><line x1="5" y1="12" x2="19" y2="12"/>'}</svg>${ic?'En carrito':'Agregar'}</button></div></div>`; }).join(''); }
function filt(c, btn) { cf = c; saveCategoryToStorage(); document.querySelectorAll('.chip').forEach(x => x.classList.remove('on')); btn.classList.add('on'); render(); document.getElementById('catalogo').scrollIntoView({behavior:'smooth'}); }
function doSearchDebounced() { clearTimeout(debounceTimer); debounceTimer = setTimeout(() => { st = document.getElementById('si').value.toLowerCase().trim(); render(); }, 300); }
function add(n, price, idx) { if (cart[n]) cart[n].qty++; else cart[n] = { n, price, qty: 1, img: P[idx].img, c: P[idx].c }; saveCartToStorage(); badge(); toast('🎲 ' + n + ' agregado'); const b = document.getElementById('cb'); b.classList.remove('pop'); void b.offsetWidth; b.classList.add('pop'); render(); }
function chg(n, d) { if (!cart[n]) return; cart[n].qty += d; if (cart[n].qty <= 0) delete cart[n]; saveCartToStorage(); badge(); renderD(); render(); }
function clearCart() { cart = {}; saveCartToStorage(); badge(); renderD(); render(); }
function badge() { const t = Object.values(cart).reduce((s,i) => s + i.qty, 0); ['cc','dc'].forEach(id => document.getElementById(id).textContent = t); }
function total() { return Object.values(cart).reduce((s,i) => s + i.price * i.qty, 0); }
function discountedTotal() { const sub = total(); if (!activeCoupon) return sub; return Math.round(sub * (1 - activeCoupon.pct / 100)); }
function updateTotals() { const sub = total(), fin = discountedTotal(); document.getElementById('st').textContent = `Bs ${sub}`; const dr = document.getElementById('discRow'); if (activeCoupon) { dr.style.display = 'flex'; document.getElementById('discAmt').textContent = `-Bs ${sub - fin}`; } else dr.style.display = 'none'; document.getElementById('gt').textContent = `Bs ${fin}`; }
function renderD() { const el = document.getElementById('di'), ft = document.getElementById('df'), items = Object.values(cart); if (!items.length) { el.innerHTML = '<div class="d-empty"><svg viewBox="0 0 24 24"><path d="M6 2 3 6v14a2 2 0 0 0 2 2h14a2 2 0 0 0 2-2V6l-3-4z"/><line x1="3" y1="6" x2="21" y2="6"/><path d="M16 10a4 4 0 0 1-8 0"/></svg><h3>Carrito vacío</h3><p>¡Agregá juegos para armar tu pedido!</p></div>'; ft.style.display = 'none'; return; } el.innerHTML = items.map(item => `<div class="ci"><div class="ci-thumb" style="background-image:url(${item.img}); background-size:cover;"></div><div class="ci-info"><div class="ci-name">${item.n}</div><div class="ci-unit">Bs ${item.price} c/u</div></div><div class="ci-price">Bs ${item.price * item.qty}</div><div class="qty"><button class="qb m" onclick="chg('${item.n.replace(/'/g,"\\'")}', -1)">−</button><span class="qn">${item.qty}</span><button class="qb" onclick="chg('${item.n.replace(/'/g,"\\'")}', 1)">+</button></div></div>`).join(''); ft.style.display = 'block'; updateTotals(); }
function openCart() { renderD(); document.getElementById('ovl').classList.add('on'); document.body.style.overflow = 'hidden'; }
function closeCart() { document.getElementById('ovl').classList.remove('on'); document.body.style.overflow = ''; }
function closeOnBg(e) { if (e.target === document.getElementById('ovl')) closeCart(); }
function sendWA() { const items = Object.values(cart); if (!items.length) return; const fin = discountedTotal(), sub = total(); const cpnLine = activeCoupon ? `\n\n🏷️ *Cupón ${activeCoupon.code}: -${activeCoupon.pct}%*\nDescuento: -Bs ${sub - fin}` : ''; const msg = `¡Hola Aynigames! 🎲 Quisiera hacer este pedido:\n\n${items.map(i => `• ${i.n} x${i.qty} — Bs ${i.price * i.qty}`).join('\n')}${cpnLine}\n\n💰 *TOTAL: Bs ${fin}*\n\n¿Pueden confirmar disponibilidad?`; window.open(`https://wa.me/59178933669?text=${encodeURIComponent(msg)}`, '_blank'); }
function sendWAConsulta() { window.open(`https://wa.me/59178933669?text=${encodeURIComponent('¡Hola Aynigames! Quisiera consultar sobre sus juegos de mesa 🎲')}`, '_blank'); }
function toast(msg) { const w = document.getElementById('tw'), el = document.createElement('div'); el.className = 'toast'; el.innerHTML = `<svg viewBox="0 0 24 24"><polyline points="20 6 9 17 4 12"/></svg>${msg}`; w.appendChild(el); setTimeout(() => { el.classList.add('out'); setTimeout(() => el.remove(), 260); }, 2500); }
const COUPONS = { AYNIGAMES10: 10, BIENVENIDO15: 15, JUEGOS5: 5 };
function applyCoupon() { const code = document.getElementById('cpnInput').value.trim().toUpperCase(); const res = document.getElementById('cpnResult'); if (!code) { res.innerHTML = ''; activeCoupon = null; updateTotals(); return; } if (COUPONS[code]) { activeCoupon = { code, pct: COUPONS[code] }; res.innerHTML = `<div class="discount-row"><span>✅ ${code} (${COUPONS[code]}% OFF)</span><button onclick="removeCoupon()">✕</button></div>`; toast('🎉 Cupón aplicado: ' + COUPONS[code] + '% de descuento'); } else { res.innerHTML = `<div style="color:#dc2626;font-size:.8rem;font-weight:600;padding:.3rem 0">❌ Cupón inválido</div>`; activeCoupon = null; } updateTotals(); }
function removeCoupon() { activeCoupon = null; document.getElementById('cpnInput').value = ''; document.getElementById('cpnResult').innerHTML = ''; updateTotals(); }
function openPM(idx) { const p = P[idx]; const ic = !!cart[p.n]; const [pl, ag, tm] = INFO[p.c]; document.getElementById('pmBox').innerHTML = `<div class="pm-img"><img src="${p.img}" alt="${p.n}"><button class="pm-close" onclick="document.getElementById('pmOvl').classList.remove('on')"><svg viewBox="0 0 24 24"><line x1="18" y1="6" x2="6" y2="18"/><line x1="6" y1="6" x2="18" y2="18"/></svg></button></div><div class="pm-body"><span class="pm-cat badge ${BC[p.c]}">${CL[p.c]}${p.new?' &nbsp;·&nbsp; <span class="badge bn">Nuevo</span>':''}</span><div class="pm-name">${p.n}</div><div class="pm-price"><small>Bs </small>${p.p}</div><div class="pm-tags"><span class="pm-tag"><svg viewBox="0 0 24 24"><path d="M17 21v-2a4 4 0 0 0-4-4H5a4 4 0 0 0-4 4v2"/><circle cx="9" cy="7" r="4"/></svg>${pl}</span><span class="pm-tag"><svg viewBox="0 0 24 24"><circle cx="12" cy="12" r="10"/><line x1="12" y1="8" x2="12" y2="12"/><line x1="12" y1="16" x2="12.01" y2="16"/></svg>${ag}</span><span class="pm-tag"><svg viewBox="0 0 24 24"><circle cx="12" cy="12" r="10"/><polyline points="12 6 12 12 16 14"/></svg>${tm}</span></div><div class="pm-desc-title">Descripción</div><div class="pm-desc">${DESC[p.c]}</div><button class="pm-add${ic?' ok':''}" onclick="add('${p.n.replace(/'/g,"\\'")}',${p.p},${idx});document.querySelector('.pm-add').className='pm-add ok';document.querySelector('.pm-add').innerHTML='<svg viewBox=\'0 0 24 24\'><polyline points=\'20 6 9 17 4 12\'/></svg>Agregado al carrito'"><svg viewBox="0 0 24 24">${ic?'<polyline points="20 6 9 17 4 12"/>':'<line x1="12" y1="5" x2="12" y2="19"/><line x1="5" y1="12" x2="19" y2="12"/>'}</svg>${ic?'Agregado al carrito':'Agregar al carrito'}</button></div>`; document.getElementById('pmOvl').classList.add('on'); document.body.style.overflow = 'hidden'; }
function closePM(e) { if (e.target === document.getElementById('pmOvl')) { document.getElementById('pmOvl').classList.remove('on'); document.body.style.overflow = ''; } }
const SLIDES_EL = () => document.querySelectorAll('.slide'); let slIdx = 0, slTimer; function slGo(n) { const s = SLIDES_EL(); s[slIdx].classList.remove('active'); slIdx = (n + s.length) % s.length; s[slIdx].classList.add('active'); document.querySelectorAll('.sl-dot').forEach((d,i)=>d.classList.toggle('on',i===slIdx)); } function slMove(d) { slGo(slIdx + d); resetTimer(); } function resetTimer() { clearInterval(slTimer); slTimer = setInterval(()=>slMove(1), 5500); } function initSlider() { const d = document.getElementById('slDots'); SLIDES_EL().forEach((_,i)=>{const b=document.createElement('button');b.className='sl-dot'+(i===0?' on':'');b.onclick=()=>{slGo(i);resetTimer();};d.appendChild(b);}); resetTimer(); }
window.addEventListener('scroll', () => document.getElementById('hdr').classList.toggle('scrolled', scrollY > 10));
document.getElementById('si').addEventListener('input', doSearchDebounced);
loadCartFromStorage();
render();
initSlider();
</script>

<!-- ========== SECCIÓN DE SUGERENCIAS PARA IMÁGENES PROFESIONALES ========== -->
<details style="max-width:1360px; margin:2rem auto; padding:1rem 2rem; background:#fff3e0; border-radius:16px; border-left:6px solid var(--w); font-family:'Inter',sans-serif;">
  <summary style="font-weight:800; font-size:1rem; cursor:pointer; color:var(--w);">📸 Recomendaciones profesionales para las imágenes del catálogo</summary>
  <div style="margin-top:1rem; font-size:0.9rem; line-height:1.6; color:#2d2d2d;">
    <p><strong>✅ Las imágenes actuales (postimg.cc + Unsplash para Spot It) son correctas para pruebas y prototipos.</strong> Sin embargo, para un catálogo profesional definitivo te sugiero:</p>
    <ul style="margin-left:1.5rem; margin-top:0.5rem;">
      <li><strong>Usar fotos reales de tus productos</strong> – nada genera más confianza que ver el juego físico (caja, componentes).</li>
      <li><strong>Fondo neutro o estudio casero</strong> – coloca el juego sobre una superficie blanca o madera clara, con luz natural difusa. Evita sombras duras.</li>
      <li><strong>Relación de aspecto uniforme</strong> – todas las imágenes deben ser 1:1 (cuadradas) o 4:3, con dimensiones mínimas de 800x800px.</li>
      <li><strong>Optimización web</strong> – comprime las imágenes (herramientas como TinyPNG o Squoosh) para que pesen menos de 200KB, manteniendo calidad.</li>
      <li><strong>Alternativa con IA (si no tienes fotos)</strong> – puedes generar imágenes estilo «caja de juego» con Midjourney o DALL·E, pero siempre añade un sello «imagen referencial» para evitar engaños.</li>
      <li><strong>Para los juegos Spot It</strong> – actualmente usan una imagen genérica de cartas. Reemplázalas por las versiones específicas (cada variante tiene su propio arte).</li>
    </ul>
    <p style="margin-top:1rem; background:#fce4d6; padding:0.75rem; border-radius:12px;"><strong>🚀 Acción recomendada:</strong> Sustituye las URLs de las imágenes por tus propias fotos alojadas en un servicio rápido (Cloudinary, Imgur, o tu propio servidor). Mantén el diseño actual, solo cambia la propiedad <code>img</code> en el array <code>P</code>.</p>
  </div>
</details>
</body>
</html>
