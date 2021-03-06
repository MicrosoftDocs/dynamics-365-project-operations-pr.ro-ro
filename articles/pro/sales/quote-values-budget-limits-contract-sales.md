---
title: Informații rezumative despre o ofertă de proiect (vânzări)
description: Acest subiect oferă informații despre informațiile și setările care se aplică și care au impact asupra ofertelor de proiect. (Sales)
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: d050258ae457bb4392d5fa761442cfc7a444feb0
ms.sourcegitcommit: f6509f7d50de4d4ebb92c1bf2cfcdf09f17458eb
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 10/06/2020
ms.locfileid: "3966845"
---
# <a name="summary-information-on-a-project-quote-sales"></a>Informații rezumative despre o ofertă de proiect (vânzări)

_**Se aplică la:** implementare simplificată - facturare de la tranzacție la proforma_

Acest articol explică informațiile care se aplică unei estimări de proiect. Aceasta include setările care au impact asupra tuturor liniilor de ofertă și informații despre ofertă care sunt rezumate pe toate elementele rând pentru a conduce KPI-urile ofertei proiectului.

Următorul tabel listează câmpurile de informații rezumative dintr-o ofertă de proiect care sunt unice pentru Dynamics 365 Project Operations sau care au unele modificări importante în comportament din ofertele Dynamics 365 Sales.

| **Câmp** | **Locaţie** | **Relevanță, scop și îndrumare** | **Impactul din aval** |
| --- | --- | --- | --- |
| Tip | Fila Rezumat (ascuns) | Acest câmp hash de set de opțiuni are următoarele opțiuni:</br>- Pe bază de muncă (disponibil numai când este instalat Project Operations)</br>- Pe bază de element (disponibil numai atunci când sunt instalate Project Operations și Vânzări)</br>- Serviciu bazat pe întreținere (disponibil când este instalat Dynamics 365 Field Service) | Când utilizați aplicația Project Operations, valoarea câmpului este setată automat la **Bazat pe muncă**. Aceasta clasifică oferta ca fiind o ofertă bazată pe proiect. O ofertă ar trebui să fie bazată pe proiect pentru a permite toate funcțiile și extensiile specifice proiectului. |
| Client potențial | Filă rezumat | Trimitere la compania clientului sau la înregistrarea contului. Când o ofertă este creată dintr-o oportunitate, acest câmp este copiat din câmpul corespunzător de pe oportunitate. | Moneda din cotația proiectului este implicită în funcție de moneda clientului. Cu toate acestea, acest lucru se poate schimba înainte ca oferta să fie salvată. |
| Manager de cont | Filă rezumat | Numele managerului de cont pentru această tranzacție. Când o ofertă este creată dintr-o oportunitate, acest câmp este copiat din câmpul corespunzător de pe oportunitate. | Managerul de cont este responsabil pentru gestionarea relației cu clientul prin finalizarea acestui proiect. Pe baza înregistrării resursei rezervabile legată de Managerul de cont, unitatea contractantă este implicită pe oferta de proiect. |
| Unitate contractantă | Filă rezumat | Unitatea de organizație care este responsabilă pentru livrarea proiectului sau proiectelor asociate acestei oferte. Când o ofertă este creată dintr-o oportunitate, acest câmp este copiat din câmpul corespunzător de pe oportunitate. | Unitatea contractantă este divizia companiei care va exeecuta proiectele după încheierea tranzacției. Fiecare unitate contractantă are o monedă, iar această monedă este utilizată pentru a raporta costurile estimate și reale suportate în timpul execuției proiectului. |
| Listă de prețuri de produse | Filă rezumat | Aceasta este lista de prețuri care este utilizată pentru stabilirea prețurilor implicite pe liniile de ofertă bazate pe produse. Lista de opțiuni pentru acest câmp afișează o listă de liste de prețuri în care moneda listei de prețuri se potrivește cu moneda din ofertă. Când o ofertă este creată dintr-o oportunitate, acest câmp este copiat din câmpul corespunzător de pe oportunitate. Acest câmp din oportunitate este implicit din înregistrarea contului, dar poate fi modificat. | Când o ofertă este câștigată, valoarea de câmp este copiată în contractul de proiect creat. |
| Monedă | Filă rezumat | Aceasta indică moneda care va fi utilizată pentru raportarea valorii acestei tranzacții. Aceasta este, de asemenea, moneda în care clientul va fi facturat dacă este câștigată tranzacția. Când o ofertă este creată dintr-o oportunitate, acest câmp este copiat din câmpul corespunzător de pe oportunitate. Acest câmp din oportunitate este în mod implicit din înregistrarea contului, dar poate fi modificat de către utilizator. | După salvarea unei oferte, acest câmp nu mai poate fi modificat. Aceasta se utilizează pentru ca pe ofertă să fie produsul implicit și listele de preț de proiect. Pe ofertă este utilizată moneda care să corespundă celei de pe lista de prețuri. |
| Limită de nedepășire | Filă rezumat | Aceasta indică limita negociată pentru valoarea finală pe care clientul este de acord pentru această tranzacție. | Această limită este evaluată în timpul execuției și se aplică tuturor elementelor rând și proiectelor asociate acestei oferte. |
| Dată solicitată pentru livrare | Filă rezumat | Când o ofertă este creată dintr-o oportunitate, acest câmp este copiat din câmpul corespunzător de pe oportunitate. | Această dată este utilizată ca dată de încheiere pentru generarea programelor de facturare. |

Mai jos sunt filele și KPI-urile disponibile pe o ofertă de proiect care sunt unice pentru operațiunile de proiect sau care au unele modificări importante în comportament din ofertele de vânzări:

| **Câmp** | **Locaţie** | **Relevanță, scop și îndrumare** |
| --- | --- | --- |
| Analiza de profitabilitate | Filă pe ofertă | Fila afișează următoarele măsurători:</br>- Cost total aplicabil</br></br>- Cost total neaplicabil</br>- Venit total</br>- Venit total (de bază)</br>- Marjă brută</br>- Marjă brută ajustată|
| Comparație cu așteptările clienților | Filă pe ofertă | Această filă afișează următoarele măsurători:</br>- Finalizare estimată</br>- Finalizare solicitată</br>- Buget client</br>- Valoare ofertă |
| Analiză de ofertă | Filă pe ofertă | Această filă rezumă următoarele KPI-uri de top pentru o ofertă de proiect</br>- Comparație cu așteptările clienților pentru buget și planificare</br>- Marjă brută</br>- Marjă brută ajustată |
