# raksonnn.github.io
import streamlit as st

# 1. Nastavitev strani (Mora biti čisto na vrhu)
st.set_page_config(
    page_title="Računanje poti in vožnje po slovenskih cestah",
    page_icon="🚗",
    layout="wide"
)

# 2. Stranski meni za navigacijo (Izpolnjevanje pogoja glede jasne navigacije)
st.sidebar.title("Navigacija")
izbira_strani = st.sidebar.radio(
    "Izberite stran:",
    ["Izračun poti", "Navodila in informacije", "Politika zasebnosti", "O nas & Kontakt"]
)

# --- STRAN 1: GLAVNA APLIKACIJA ---
if izbira_strani == "Izračun poti":
    st.title("🚗 Računanje poti in vožnje po slovenskih cestah")
    st.subheader("Pametno načrtovanje potovanja in stroškov vožnje")
    
    # Tukaj vstavite vašo obstoječo logiko za izračun poti
    st.info("V spodnja polja vnesite podatke za izračun optimalne poti.")
    
    # PRIMER VAŠE OBSTOJEČE KODE:
    # zacetek = st.text_input("Začetno mesto")
    # cilj = st.text_input("Cilj")
    # if st.button("Izračunaj"):
    #     ... vaša koda ...
    
    st.write("---")
    # SEO Besedilo pod aplikacijo (Google potrebuje besedilo za analizo!)
    st.markdown("""
    ### Zakaj uporabiti naš načrtovalec poti?
    Naša spletna aplikacija omogoča natančno **računanje poti**, predvidenega časa vožnje in porabe goriva za potovanja po Sloveniji. 
    Ne glede na to, ali potujete iz Ljubljane v Maribor ali raziskujete skrite kotičke Primorske, vam naš iskalnik pomaga optimizirati pot.
    """)

# --- STRAN 2: NAVODILA IN INFORMACIJE (Dodana vsebina za Google) ---
elif izbira_strani == "Navodila in informacije":
    st.title("ℹ️ Kako deluje izračunavanje poti?")
    st.write("""
    Aplikacija uporablja napredne podatke o slovenskih cestah za izračun najhitrejše poti. 
    Pri načrtovanju upoštevajte naslednje nasvete:
    * **Cestnine in vinjete:** Za vožnjo po slovenskih avtocestah potrebujete veljavno e-vinjeto.
    * **Poraba goriva:** Izračun porabe je informativne narave in se lahko razlikuje glede na vaš stil vožnje ter vrsto vozila.
    * **Prometne informacije:** Pred odhodom vedno preverite trenutno stanje na cestah preko uradnih servisov (npr. PIC).
    """)

# --- STRAN 3: POLITIKA ZASEBNOSTI (Nujno za AdSense!) ---
elif izbira_strani == "Politika zasebnosti":
    st.title("🔒 Politika zasebnosti (Privacy Policy)")
    st.markdown(f"""
    Zadnja posodobitev: September 2026
    
    Na spletni strani **Računanje poti** cenimo vašo zasebnost. Ta dokument opisuje, katere podatke zbiramo in kako jih uporabljamo.
    
    ### 1. Zbiranje podatkov
    Aplikacija ne shranjuje vaših osebnih podatkov ali lokacij iskanja. Vsi izračuni se izvajajo v realnem času.
    
    ### 2. Piškotki in oglaševanje
    Uporabljamo storitev **Google AdSense** za prikazovanje oglasov. Google kot zunanji ponudnik uporablja piškotke za prikazovanje oglasov na podlagi vaših obiskov te in drugih spletnih strani. Uporabniki lahko piškotke onemogočijo v nastavitvah svojega brskalnika.
    """)

# --- STRAN 4: O NAS & KONTAKT (Dokazovanje legitimnosti) ---
elif izbira_strani == "O nas & Kontakt":
    st.title("📬 O nas in kontaktni podatki")
    st.write(""" 069408006""")
    Spletna aplikacija je nastala z namenom olajšati načrtovanje poti in stroškov vožnje po Sloveniji. 
    Razvita je v okolju Python z uporabo knjižnice Streamlit.
    
    **Kontakt za podporo in vprašanja:**
    * **E-pošta:** vas-email@domena.com (Zamenjajte s svojim pravim e-naslovom)
    """)
    
