<template>
  <Container>
    <TitresH1> Accueil </TitresH1>

    <TextesParagraphe> Bienvenue sur le site. </TextesParagraphe>

    <TitresH2> Documentation </TitresH2>
    <ListsGrid>
      <li>
        <CardsIconCard to="/docs/composants">
          <template #icon>
            <i
              class="ri-ghost-smile-line text-[#001B79] group-hover:text-[#FF55BB]"
            ></i>
          </template>
          Composants
        </CardsIconCard>
      </li>

      <li>
        <CardsIconCard to="/docs/layouts">
          <template #icon>
            <i
              class="ri-aliens-line text-[#001B79] group-hover:text-[#FF55BB]"
            ></i>
          </template>
          Layouts
        </CardsIconCard>
      </li>

      <li>
        <CardsIconCard to="/docs/icones">
          <template #icon>
            <i class="ri-bear-smile-line text-[#001B79] group-hover:text-[#FF55BB]"></i>
          </template>
          Icones
        </CardsIconCard>
      </li>
    </ListsGrid>
  </Container>
</template>
