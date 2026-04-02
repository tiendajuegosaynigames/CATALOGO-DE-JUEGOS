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
.d
