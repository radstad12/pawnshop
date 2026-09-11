# POINTO LLC — Pawnshop app

Hotový starter pro veřejný výkupní katalog + zabezpečenou administraci.

## Co umí
- veřejný katalog bez zobrazení cen
- zákazník zadá počet kusů a dostane celkovou orientační částku
- bonusové prahy (např. nad 1 000 $ +5 %)
- admin přihlášení přes Supabase Auth (e-mail + heslo)
- admin může přidávat mazat a skrývat produkty a nastavovat výkupní ceny
- ceny se veřejnému klientovi neposílají; kalkulace běží přes bezpečnou Supabase RPC funkci
- neon fialovo-zlatý POINTO design a logo v `public/logo.png`

## 1. Supabase
1. Vytvoř projekt na Supabase.
2. V SQL Editoru spusť `supabase/schema.sql`.
3. V Authentication vytvoř admin účet (e-mail + heslo). Registraci pro veřejnost nech vypnutou.
4. Zkopíruj `.env.example` na `.env.local` a doplň URL + anon key.

## 2. Lokálně
```bash
npm install
npm run dev
```

## 3. GitHub + Vercel
Repo můžeš připojit přímo do Vercelu. Po každém pushi se projekt automaticky znovu nasadí. V nastavení Vercelu přidej stejné environment variables:
- `VITE_SUPABASE_URL`
- `VITE_SUPABASE_ANON_KEY`

## Poznámka
Toto je funkční MVP základ. Pro ostrý provoz bych ještě přidal audit log změn cen, upload obrázků produktů přes Supabase Storage, více admin rolí a potvrzení nabídky/objednávky.
