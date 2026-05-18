---
id: serverSideFormValidation
title: "Exemple serverSideFormValidation | Bonnes pratiques avec Refine v5"
display_title: "Validation de formulaire côté serveur"
sidebar_label: "Validation côté serveur"
description: "Construisez une validation de formulaire côté serveur dans Refine v5. Découvrez les étapes clés et les bonnes pratiques de composants UI d'entreprise pour des panels d'administration React réels."
example-tags: [form, antd]
---

Vous pouvez gérer les erreurs de validation côté serveur directement avec [Ant Design useForm](/core/docs/ui-integrations/ant-design/hooks/use-form).

Lorsque `dataProvider` renvoie une promesse rejetée avec un champ `errors`, [`useForm`](/core/docs/ui-integrations/ant-design/hooks/use-form) met automatiquement à jour l'état d'erreur avec ce champ `errors`.

[Consultez la documentation sur la validation de formulaire côté serveur pour plus d'informations. →](/core/docs/guides-concepts/forms/#server-side-validation-)

<CodeSandboxExample path="server-side-form-validation-antd" />
